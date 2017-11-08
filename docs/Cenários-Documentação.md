Autor: Kairon Velozo

***
### C1 - Criar Páginas na Wiki
| | |
| ------------- | ------------- |
| **Objetivo** | Criação de páginas na _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki) do [repositório remoto]()_ |
| **Contexto** | Gerenciamento de documentação do projeto |
| **Atores** | [Colaborador]() |
| **Recursos** | Título da página  |
|| Conteúdo da página  |
|| Mensagem de alteração (opcional)
| **Exceções** | Existência prévia de uma página com o mesmo título |
| **Episódios** | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa o repositório do projeto.
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki)_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _New Page_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) preenche as informações de título e conteúdo da página
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) fornece uma mensagem de alteração (opcional)
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em Save Page |
### C2 - Editar Páginas da Wiki
| | |
| ------------- | ------------- |
| **Objetivo** | Alteração de informações e conteúdo de páginas existentes na _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki) do [repositório remoto](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#reposit%C3%B3rio-remoto)_ |
| **Contexto** | Gerenciamento de documentação do projeto |
| **Atores** | [Colaborador]() |
| **Recursos** | Título da página |
|| Conteúdo da página  |
|| Mensagem de alteração (opcional)
| **Exceções** | Alteração para um título de página já utilizado por outra página |
| **Episódios** | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa o repositório do projeto.
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki)_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa a página desejada através do menu lateral
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _Edit Page_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) altera as informações de título e/ou conteúdo da página
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) fornece uma mensagem de alteração (opcional)
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em Save Page |
### C3 - Acessar Conteúdo de Páginas da Wiki
| | |
| ------------- | ------------- |
| **Objetivo** | Visualizar o conteúdo de páginas existentes na _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki) do [repositório remoto](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#reposit%C3%B3rio-remoto)_ |
| **Contexto** | Gerenciamento de documentação do projeto |
| **Atores** | [Colaborador](), [Visitante]() |
| **Recursos** | Página |
| **Exceções** | Tentar acessar uma página existente |
| **Episódios** | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa o repositório do projeto.
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki)_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa a página desejada através do menu lateral
### C4 - Exclusão Páginas da Wiki
| | |
| ------------- | ------------- |
| **Objetivo** | Excluir páginas existentes na _[WIki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki) do [repositório remoto](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#reposit%C3%B3rio-remoto)_ |
| **Contexto** | Gerenciamento de documentação do projeto |
| **Atores** | [Colaborador]() |
| **Recursos** | Página |
| **Exceções** | Tentar excluir uma página inexistente |
| **Episódios** | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa o repositório do projeto.
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki)_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa a página desejada através do menu lateral
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _Edit Page_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _Delete Page_ e confirma a ação no _popup_
### C5 - Comparar Versões de uma Páginas da Wiki
| | |
| ------------- | ------------- |
| **Objetivo** | Rastrear alterações de uma página da _[WIki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki) do [repositório remoto](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#reposit%C3%B3rio-remoto)_ |
| **Contexto** | Gerenciamento de documentação do projeto |
| **Atores** | [Colaborador](), [Visitante]() |
| **Recursos** | Página |
| **Exceções** | Inexistência de múltiplas versões da página |
| **Episódios** | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa o repositório do projeto.
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki)_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa a página desejada através do menu lateral
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _revisions_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) seleciona, através dos checkboxes, as versões desejadas da página
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _Compare Revisions_
### C6 - Buscar Páginas da Wiki
| | |
| ------------- | ------------- |
| **Objetivo** | Localização especifica de páginas da _[WIki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki) do [repositório remoto](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#reposit%C3%B3rio-remoto)_ |
| **Contexto** | Gerenciamento de documentação do projeto |
| **Atores** | [Colaborador](), [Visitante]() |
| **Recursos** | Título da página |
| **Exceções** | Inexistência de páginas para o termo buscado |
| **Episódios** | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) acessa o repositório do projeto.
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _[Wiki](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#wiki)_
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) clica em _Pages_ no menu lateral
| | O [colaborador](https://github.com/github-requirements/docs/wiki/L%C3%A9xicos#colaborador) preenche informa o título da página (termo de busca) na caixa de texto
