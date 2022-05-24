# Interpreter

The bot has its own code interpreter, this allows you to customize a large part of its modalities.

## What is it?
It is by saying its own "language" to interpret text. This allows you to use things that are not yet known, such as the names of new users on the server.
Can be used in: Tags, Welcome, Leave, Boost and some other commands.
## Even easier...
If at the time of establishing our welcome message (`t!welcome message`) we write in a part **`{user.name}`** this text will be replaced with the name of the new user who has joined, or **`{server.name}`** to the name of the server.
## Testing the interpreter
You can test the interpreter by using `t!test` command
![image](https://user-images.githubusercontent.com/83442808/169927312-d5fe4dea-9e89-4a98-a0b5-fc5b4487acdb.png)
## Full list (Variables):

|     Server         |      Description              |     User              |      Description             |
|--------------------|-------------------------------|-----------------------|------------------------------|
| `{server.id}`      |  Server ID                    | `{user.id}`           |  User ID                     |
| `{server.name}`    |  Server Name                  | `{user.name}`         |  User name                   |
| `{server.icon}`    |  Server icon URL              | `{user.avatar}`       |  User avatar URL             |
| `{server.members}` |  Server members count         | `{user.tag}`          |  User tag                    |
| `{server.boosts}`  |  Server boosts count          | `{user.mention}`      |  User mention                |
| `{server.owner.id}`|  Server owner ID              | `{user.discriminator}`|  User discriminator          |

## Functions
Functions are practically the same as variables, only they need to have something to work

## Example
If in a part of our welcome message we write **`{random:thing1,thing2,thing3,...}`** this text will be replaced to a random thing from those provided (The separator is `,`)
## Full list (Functions):
|     Nombre      |     Description                             |     Ussag                   |     Example           |
|-----------------|---------------------------------------------|-----------------------------|-----------------------|
| `{random:}`     |Returns a random element from those provided | `{random:thing1,thing2,...}`|`{random:yes,no,maybe}`|
| `{number:}`     |Returns a random number between two provided | `{number:min,max}`          |`{number:1,100}`       |

## Embeds
An __embed__ is a message with a "box" that can be sent on discord, example of an embed:

![Demo](https://cdn.discordapp.com/attachments/778156886553395210/978451087226970142/unknown.png)

__***Syntax:***__
> **`*`**: Required
> **`?`**: Optional

## Full list (Embeds):
|       Usage           |       Example                 |
|-----------------------|-------------------------------|
|`{title:text*}`        |`{title:My title}`             |
|`{description:text*}`  |`{description:Mi description}` |
|`{image:URL*}`         |`{image:https://...}`          |
|`{thumbnail:URL*}`     |`{thumbnail:https://...}`      |
|`{color:Hex code*}`    |`{color:#0000ff}`              |
|`{author:text*,URL?}`  |`{author:Mid,https://...}`     |
|`{footer:text*,URL?}`  |`{footer:My footer}`           |

## Conclusion
You can use all this (Variables, Functions and Embeds) to customize your messages of the __Tags, Welcome, Leave or Boost Alerts__ modalities to your liking.

## Examples
**Code:**
```
{description:**{USER.TAG}** just boosted the server!}{author:{USER.TAG},{USER.AVATAR}}{color:#0000ff}{image:https://api.miduwu.ga/image/boost?image={USER.AVATAR}}{footer:{SERVER.NAME},{SERVER.ICON}}
```
**Result:**

![image](https://user-images.githubusercontent.com/83442808/169929627-531dec0a-2138-4a66-96c3-8575109ad6c4.png)
