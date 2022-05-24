# Interpretador

O bot possui um interpretador de código próprio, o que permite personalizar grande parte de suas modalidades.

## O que é isso?
É dizendo sua própria "linguagem" para interpretar o texto. Isso permite que você use coisas que ainda não são conhecidas, como os nomes de novos usuários no servidor.
Pode ser usado em: Tags, Welcome, Leave, Boost e alguns outros comandos.
## Ainda mais fácil...
Se no momento de estabelecer nossa mensagem de boas-vindas (`t!welcome message`) escrevermos em uma parte **`{user.name}`** este texto será substituído pelo nome do novo usuário que ingressou, ou **`{server.name}`** para o nome do servidor.
## Testando o interpretador
Você pode testar o interpretador usando o comando `t!test`
![image](https://user-images.githubusercontent.com/83442808/169930353-d40f34c1-357d-479d-a04d-1792a95b6fad.png)
## Lista completa (variáveis):

|     Servidor         |      Descrição                 |     Usuário           |      Descrição             |
|--------------------|----------------------------------|-----------------------|----------------------------|
| `{server.id}`      |  ID do servidor                  | `{user.id}`           |  ID do usuário             |
| `{server.name}`    |  Nome do servidor                | `{user.name}`         |  Nome do usuário           |
| `{server.icon}`    |  URL do ícone do servidor        | `{user.avatar}`       |  URL do avatar do usuário  |
| `{server.members}` |  Contagem de membros do servidor | `{user.tag}`          |  Tag do usuario            |
| `{server.boosts}`  |  Contagem de boosts do servidor  | `{user.mention}`      |  Menção do usuário         |
| `{server.owner.id}`|  ID do proprietário do servidor  | `{user.discriminator}`|  Discriminador de usuário  |

## Funções
As funções são praticamente iguais às variáveis, só que precisam ter algo para funcionar

## Exemplo
Se em uma parte da nossa mensagem de boas-vindas escrevermos **`{random:coisa1,coisa2,coisa3,...}`** este texto será substituído por uma coisa aleatória daquelas fornecidas (O separador é `,`)
## Lista completa (Funções):
|     Nome      |     Descrição                                      |     Uso                      |     Exemplo             |
|-----------------|--------------------------------------------------|------------------------------|-------------------------|
| `{random:}`     |Retorna um elemento aleatório daqueles fornecidos | `{random:coisa1,coisa22,...}`|`{random:sim,não,talvez}`|
| `{number:}`     |Retorna um número aleatório entre dois fornecidos | `{number:min,max}`           |`{number:1,100}`         |

## Embeds
Um __embed__ é uma mensagem com uma "caixa" que pode ser enviada no discord, exemplo de um embed:

![image](https://user-images.githubusercontent.com/83442808/169933761-8d2bfd6a-3b48-4aad-9dec-7f6bb58682e5.png)

__***Sintaxe:***__
> **`*`**: Requerido
> **`?`**: Opcional
## Lista completa (Incorporação):
|       Uso             |       Exemplo                 |
|-----------------------|-------------------------------|
|`{title:texto*}`       |`{title:My title}`             |
|`{description:texto*}` |`{description:Mi description}` |
|`{image:URL*}`         |`{image:https://...}`          |
|`{thumbnail:URL*}`     |`{thumbnail:https://...}`      |
|`{color:Código hex*}`  |`{color:#0000ff}`              |
|`{author:texto*,URL?}` |`{author:Mid,https://...}`     |
|`{footer:texto*,URL?}` |`{footer:My footer}`           |

## Conclusão
Você pode usar tudo isso (Variáveis, Funções e Embeds) para personalizar suas mensagens das modalidades __Tags, Welcome, Leave ou Boost Alerts__ ao seu gosto.

## Exemplos
**Code:**
```
{description:**{USER.TAG}** acabou de impulsionar o servidor!}{author:{USER.TAG},{USER.AVATAR}}{color:#0000ff}{image:https://api.miduwu.ga/image/boost?image={USER.AVATAR}}{footer:{SERVER.NAME},{SERVER.ICON}}
```
**Resultado:**

![image](https://user-images.githubusercontent.com/83442808/169934438-e4b01ed5-8bf7-4d41-a1b2-ab824f6befa6.png)
