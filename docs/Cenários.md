## Introdução
Cenário é uma aproximação utilizada na engenharia de requisitos que facilita a criação e utilização de casos de uso, de uma forma simples e flexível. A utilização desta aproximação na engenharia de requisitos é baseada na hipótese de que a integração desta técnica permite melhorar o processo de especificação de requisitos através de um maior envolvimento dos utilizadores no mesmo. Esta técnica descreve os requisitos numa linguagem fácil de entender e validar para todas as pessoas relacionadas com o projeto, motivando-as a discutir e participar, obtendo assim um maior feedback sobre o que está sendo feito.

Para o projeto desenvolvido nesse repositório utiliza os cenários justamente da forma proposta acima e os cenários são divididos em categorias descritas no módulo de ajuda do GitHub, encontrado [aqui](http://help.github.com/). Cada cenário possui diversas palavras-chave que são chamadas de léxicos. Os léxicos podem ser encontrados [aqui](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos) e cada uma destas palavras-chaves que são essenciais estão sendo referenciados em cada cenário.

## Cenários
* [Documentação](https://github.com/github-requirements/docs/wiki/Cen%C3%A1rios-Documenta%C3%A7%C3%A3o)
* [Gerenciamento de Comunidade](https://github.com/github-requirements/docs/wiki/Cen%C3%A1rios-Gerenciamento-de-Comunidade)
* [Gerenciamento de Projeto](https://github.com/github-requirements/docs/wiki/Cen%C3%A1rios-Ger%C3%AAncia-de-Projetos)
* [Revisão de Código](https://github.com/github-requirements/docs/wiki/Cen%C3%A1rios-Revis%C3%A3o-de-C%C3%B3digo)

<!-- ### Básicos do Github 
### Configuração de Ambiente
### Sobre o Github -->
### Utilizando o Git
#### 
| **Titulo**  | Ignorar arquivos e pastas (gitignore) |
| ------------- | ------------- |
| **Objetivo** | Ignorar arquivos não desejados na [repositório remoto](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#reposit%C3%B3rio-remoto) do [Git](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#git-plataforma) |
| **Contexto** | Utilização diária e configuração |
| **Atores** | Usuário; Gerente de Configuração |
| **Recursos** | Projeto, repositório |
| **Episódios** | O usuário determina quais seriam os arquivos a serem ignorados
| | O usuário cria um arquivo [.gitignore](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#gitignore) localmente
| | O usuário adiciona o caminho para os arquivos a serem ignorados no .gitignore
| | O usuário faz o [commit](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#commit) do arquivo .gitignore configurado
| | O usuário faz o [push](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#push) do [commit](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#commit) ao repositório remoto do Git |

| **Título** | Bloquear a exposição do email pessoal nos pushes do Git |
| ------------- | ------------- |
| **Objetivo** | Não expor emails pessoais durante a utilização de um [push](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#push) num repositório [Git](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#git-plataforma) |
| **Contexto** | Utilização diária e configuração |
| **Atores** | Usuário |
| **Recursos** | Projeto, repositório, [website do Github](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#github-website) |
| **Episódios** | O usuário decide-se por não expor seu email pessoal
| | O usuário abre o website do Github
| | O usuário clica na sua foto de perfil e clica em Settings
| | O usuário na barra lateral esquerda em Emails
| | O usuário clica em Keep my email address private
| | O usuário clica em Block command line pushes that expose my email |

### Criando e administrando a conta do Github
| **Título** | Obter assinatura premium para conta de usuário |
| ------------- | ------------- |
| **Objetivo** | Obter os recursos de assinatura premium na conta do usuário |
| **Contexto** | Atualização de Conta |
| **Atores** | Usuário |
| **Recursos** | Conta de usuário, planos de assinatura, cartão de crédito |
| **Episódios** | O usuário acessa a página de CONFIGURAÇÕES.
| | O usuário acessa a página de COBRANÇAS.
| | O usuário escolhe o método de pagamento (anual ou mensal).
| | O usuário informa os dados de seu cartão de crédito.
| | O usuário submete o pedido e a conta é atualizada caso o pedido esteja correto. 

<!-- ### Autenticação
### Criando e administrando o perfil do Github
### Escrevendo no Github
### Criando e configurando organizações e times
### Criando, clonando e arquivando repositórios
### Administrando arquivos em um repositório
### Administrando arquivos muito grandes
### Commitando
### Procurando por uma informação no Github
### Notificações
### Explorando projetos no Github
### Utilizando atalhos de teclado
### Colaborando com issues e pull requests
### Construindo uma comunidade consistente -->
### Administrando colaboradores de um repositório
| **Título** | Atribuir issues a outros usuários |
| ------------- | ------------- |
| **Objetivo** | Atribuir responsáveis para a solução de uma issue |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Projeto, issue, colaboradores |
| **Episódios** | O usuário acessa a página do repositório.  
| | O usuário acessa a página de issues.
| | O usuário cria uma nova issue ou seleciona uma existente.
| | O usuário procura colaboradores através de seu username, tomando em conta que é possível escolher um número máximo de colaboradores.
| | O usuário clica em “atribuir”.

<!-- ### Administrando repositório remotos
### Hospedando seus lançamentos
### Visualizando dados de um repositório e gráficos
### Importando seus projetos para o Github
### Git Avançado
### Administrando seu trabalho no Github
### Administrando um repositório
### Gists
### Wiki
### Automação -->
### Customizando seu ambiente de trabalho no Github
| **Título** | Criar um quadro de projeto |
| ------------- | ------------- |
| **Objetivo** | Criar um workflow personalizado para as necessidades do projeto. |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Projeto |
| **Episódios** | O usuário acessa a página principal do repositório.
| | O usuário acessa a página de projetos.
| | O usuário clica na opção “Novo Projeto”.
| | O usuário preenche as informações do quadro e submete o pedido.
| | O usuário cria colunas para o quadro, de acordo com as necessidades e workflow. 

<!-- ### Github Pages Básico
### Customizando seu Github Pages 
### Ensinando e aprendendo no Github Educational
### Empregos no Github
### Trabalhando com o suporte do Github -->