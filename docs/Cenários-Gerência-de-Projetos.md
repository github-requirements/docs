### C1 - Criar uma issue
| **Título** | Criar uma Issue|
| ------------- | ------------- |
| **Objetivo** | Rastrear idéias, aprimoramentos, tarefa ou erros para o projeto Github |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Título da Issue |
| **Episódios** | O usuário acessa a página principal do repositório.
| | O usuário clica em "Issues"
| | O usuário clica em "New issue"
| | O usuário digita um Título
| | O usuário clica em "Submit new issue"
| **Restrição** | Ter uma issue com um escopo bem definido. |
| **Exceção** | A issue proposta já foi feita e não foi rastreada. |
### C2 - Adicionar uma Task list
| **Título** | Adicionar uma Task list|
| ------------- | ------------- |
| **Objetivo** | Elaborar uma lista de tarefas, quebrando uma grande issue em tarefas menores|
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Ter uma issue |
| **Episódios** | O usuário acessa a página principal do repositório
| | O usuário clica em "Issues"
| | O usuário clica no ícone " Add a task list "
| | O usuário digita sua task
| | O usuário clica em "Comment"
| **Restrição** | Criar uma Task organizada e com bons nomes|
| **Exceção** | A task proposta já foi feita e não foi rastreada |

### C3 - Adicionar labels
| **Título** | Adicionar uma Label|
| ------------- | ------------- |
| **Objetivo** |  Atribuir uma característica ou tipo para a issue, possibilitando posteriormente encontrar rapidamente as issues que estão relacionadas entre si|
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Ter uma issue |
| **Episódios** | O usuário acessa a página principal do repositório
| | O usuário clica em "Issues"
| | O usuário seleciona o checkbox da issues que desejar adicionar uma label
| | O usuário clica em "Label"
| | O usuário seleciona o tipo desejado da label
| **Restrição** | Adicionar o tipo de label precisamente certo para o tipo de issue|
| **Exceção** | Adicionar uma label não apropriada para o tipo de issue |

### C4 - Criar uma milestone
| **Título** | Criar um milestone|
| ------------- | ------------- |
| **Objetivo** | Rastrear um projeto como parte de um objetivo maior |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Ter um título |
| **Episódios** | O usuário acessa a página principal do repositório
| | O usuário clica em "Issues"
| | O usuário clica em "Milestone"
| | O usuário clica em "new Milestone
| | O usuário digita um título, descrição e seleciona uma data
| | O usuário clica em "Create milestone"
| **Restrição** | O usuário ter inserido um título claro para a equipe |
| **Exceção** | O usuário adicionar um milestone não apropriado para o projeto |

### C5 - Adicionar um Assignee
| **Título** | Adicionar um Assignee|
| ------------- | ------------- |
| **Objetivo** | Atribuir até 10 companheiros de equipe um problema para garantir que a issue tem um ou vários proprietários |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Ter uma issue |
| **Episódios** | O usuário acessa a página principal do repositório.
| | O usuário clica em "Issues"
| | O usuário seleciona o checkbox da issue que deseja atribuir um proprietário
| | O usuário clica em "Assignee"
| | O usuário seleciona o futuro proprietário da issue
| **Restrição** | Atribuir precisamente os proprietários que devem assumir a issue|
| **Exceção** | Atribuir um proprietário que não tem aptidão para a issue|

### C6 - Criar uma Project Board
| **Título** | Criar uma Project Board|
| ------------- | ------------- |
| **Objetivo** | Visualizar todo o trabalho e priorizar issues ao lado do seu código, ver quais as tasks planejadas ou em andamento, seja em um repositório ou em toda a organização |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Um nome para a Project Board |
| **Episódios** | O usuário acessa a página principal do repositório.
| | O usuário clica em "Projects"
| | O usuário clica em "New Project"
| | O usuário digita um nome e se desejar descrição"
| | O usuário clica em "Save project"
| **Restrição** | A Project Board possuir um nome explicativo para o tipo de projeto e uma boa descrição |
| **Exceção** | A Project Board ser criada e os usuários não serem diligentes em utiliza-la |

### C7 - Adicionar coluna em uma Project Board
| **Título** | Adicionar coluna em uma Project Board |
| ------------- | ------------- |
| **Objetivo** | Adicionar caracteristicas de um modelo de controle de desenvolvimento, como o kanban |
| **Contexto** | Gerenciamento de Projeto |
| **Atores** | Usuário |
| **Recursos** | Um nome para a coluna |
| **Episódios** | O usuário acessa a página principal do repositório.
| | O usuário clica em "Projects"
| | O usuário clica em "Add column"
| | O usuário digita um nome para a coluna"
| | O usuário clica em "Create column"
| **Restrição** | A coluna possuir um nome explicativo para a etapa apropriada do projeto |
| **Exceção** | A coluna ser criada e os usuários não serem diligentes em utiliza-la |