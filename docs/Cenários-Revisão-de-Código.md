## Cenários relaciodados à feature _**Code Review**_ do Github
### C1 - Abrir um pull-request
| **Titulo**  | Abrir um pull-request |
| ------------- | ------------- |
| **Objetivo** | Disponibilizar alterações realizadas para visualização de outros desenvolvedores e/ou gerentes |
| **Contexto** | Após FINALIZAR alterações e realizar os PUSHs |
| **Atores** | Contribuidor |
| **Recursos** | branches, commits, arquivos |
| **Episódios** | Contribuidor realiza alterações no código ou implementa novo código em NOVA branch |
| | Contribuidor realiza commit das alterações feitas |
| | Contribuidor realiza push dos commits feitos na nova branch |
| | Contribuidor abre pull-request para avaliação do código contido na branch |
| **Restrição** | Código ter sido desenvolvido em uma branch separada da branch principal |

### C2 - Aceitar um pull-request
| **Titulo**  | Aceitar um pull-request |
| ------------- | ------------- |
| **Objetivo** | Realizar merge das alterações realizadas numa branch à branch principal |
| **Contexto** | Após um pull-request ter sido ABERTO |
| **Atores** | Colaborador |
| **Recursos** | branches, commits, arquivos, pull-request aberto |
| **Episódios** | Contribuidor e Colaborador DISCUTEM o código contido no pull-request aberto |
| | Contribuidor e Colaborador e/ou gerentes certificam-se de que o código está CORRETO |
| | Colaborador aceita o pull-request aberto |
| **Restrição** | Haver um pull-request aberto |
| | O código contido no pull-request aberto estar correto |
| **Exceção** | O código contido no pull-request aberto NÃO estar correto |

### C3 - Fechar um pull-request
| **Titulo**  | Fechar um pull-request |
| ------------- | ------------- |
| **Objetivo** | Fechar um pull-request aberto SEM REALIZAR MERGE das alteração realizadas à branch principal |
| **Contexto** | Quando código não é necessário |
| **Atores** | Colaborador |
| **Recursos** | branches, commits, arquivos, pull-request aberto |
| **Episódios** | Colaborador percebe que o código não é necessário ou que outra solução foi implementada em uma branch diferente |
| | Colaborador ou gerente fecha pull-request aberto |
| **Restrição** | Haver um pull-request aberto |
| **Exceção** | Pull-request aberto ser aceito |

### C4 - Utilizar o diff no pull-request aberto
| **Titulo**  | Utilizar o diff no pull-request aberto |
| ------------- | ------------- |
| **Objetivo** | Visualizar alterações realizadas no código contido no pull-request aberto  |
| **Contexto** | ANTES de aceitar ou fechar pull-request aberto |
| **Atores** | Colaborador  |
| **Recursos** | branches, commits, arquivos, pull-request aberto, código |
| **Episódios** | Colaborador verifica que há um pull-request aberto  |
| | Colaborador desejam visualiza as alterações realizadas pelo código contido no pull-request aberto em comparação à branch principal |
| | Colaborador clica no link "Files changed" na página do pull-request aberto |
| | Colaborador visualiza as linhas de código que foram alteradas, adicionadas ou excluídas ao código da branch principal |
| **Restrição** | Haver um pull-request aberto |

### C5 - Discutir o código do pull-request aberto
| **Titulo**  | Discutir o código do pull-request aberto |
| ------------- | ------------- |
| **Objetivo** | Certificar-se de que o código contido no pull-request aberto está correto |
| **Contexto** | ANTES de aceitar ou fechar pull-request aberto |
| **Atores** | Colaborador |
| **Recursos** | branches, commits, arquivos, pull-request aberto, código |
| **Episódios** | Colaborador verificam que há um pull-request aberto  |
| | Colaborador visualizam as alterações realizadas pelo código contido no pull-request aberto em comparação à branch principal |
| | Colaborador clicam no link "Files changed" na página do pull-request aberto |
| | Colaborador visualizam as linhas de código que foram alteradas, adicionadas ou excluídas ao código da branch principal |
| | Colaborador clicam no link para comentar a linha do código, todo o código ou requerir uma revisão |
| **Restrição** | Haver um pull-request aberto |

| **Titulo**  | Efetuar um rebase |
| ------------- | ------------- |
| **Objetivo** | Atualizar a branch corrente com uma nova versão da mesma ou de outra branch |
| **Contexto** | ANTES/DEPOIS de efetuar um push/commit |
| **Atores** | Desenvolvedores |
| **Recursos** | branches, commits |
| **Episódios** | Colaborador realiza um commit e/ou deseja realizar um push |
| | Colaborador verifica que houve ou não mudanças |
| | Colaborador realiza o rebase para atualizar sua branch com a branch de destino |

| **Titulo**  | Requerir review |
| ------------- | ------------- |
| **Objetivo** | Solicitar review de seu código no pull-request |
| **Contexto** | APÓS abrir um pull-request |
| **Atores** | Contribuidor |
| **Recursos** | branches, commits, pull-request aberto, código, arquivos |
| **Episódios** | Contribuidor abre um pull-request |
| | Contribuidor  navega até a pagina do pull-request |
| | Contribuidor ou Gerente clica no link _**Reviewers**_ |
| | Contribuidor ou Gerente digita ou clica no nome da pessoa a quem a quem será solicitada a revisão do código |
| **Restrição** | Haver um pull-request aberto |
| | A pessoa a quem será solicitada a revisão do código do pull-request aberto deve estar incluída no repositório do projeto |

---

| **Titulo**  | Utilizar blame view |
| ------------- | ------------- |
| **Objetivo** | Ver como estava um arquivo antes de uma mudança em particular   |
| **Contexto** | Código está hospedado no GitHub e foi feito uma alteração |
| **Atores** | Colaborador |
| **Recursos** | Commits |
| **Episódios** | Colaborador navega para a página principal do _repsitório_  |
| | Colaborador clica no arquivo que se quer checar história de mudanças  |
| | Colaborador clicam em _Blame_ para abrir o _blame view_ |
| **Restrição** | Ser o primeiro _commit_ |

| **Titulo**  | Resolver um conflito de _merge_ no GitHub |
| ------------- | ------------- |
| **Objetivo** | _Merjar_ pull requests resolvendo simples conflitos no GitHub  |
| **Contexto** | Foi aberto um Pull Request e o GitHub alertou que há conflitos |
| **Atores** | Desenvolvedores |
| **Recursos** | Commits, branchs, pull-request aberto |
| **Episódios** | Desenvolvedor navega para a página principal do _repsitório_  |
| | Desenvolvedor clica em Pull requests  |
| | Desenvolvedor clica na lista dos Pull requests naquele que estiver com um "x em vermelho" |
| | Desenvolvedor clica no botão "Resolve conflicts" |
| | Desenvolvedor decide o que fica e o que irá sair do código em conflito |
| | Desenvolvedor clica em "Mark as resolved" |
| **Restrição** | Haver conflitos, Haver Pull Requests abertos |
