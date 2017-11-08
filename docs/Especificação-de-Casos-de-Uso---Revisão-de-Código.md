# DOCUMENTO DE CASOS DE USOS 
## Tema: Revisão de Código | Grupo: GitHub
### Alunos responsáveis: Varley Silva e Victor Leite


## 1. Introdução
Através de uma análise profunda da equipe, foi decidido "dividir" o GitHub em funcionalidades principais (onde o próprio GitHub define essas funcionalidades principais) e cada integrante(es) da equipe ficou responsável em elaborar o Diagrama de Casos de Uso e a Especificação de Casos de Uso. Logo a funcionalidade Revisão de Código (Code Review) ficou de responsabilidade dos alunos Varley Silva e Victor Leite.


## 2. Identificação dos atores
| Ator   |      Nome do Ator      |  Descrição Ator |
|--------|:----------------------:|:----------------:|
| Ator 01 |  Colaborador | Uma pessoa que está envolvida que esta na sua organização e que possa ler, escrever ou permissões de administrador para um ou mais repositórios na sua organização.  |
| Ator 02 |    Contribuidor   |  Um colaborador é alguém que contribuiu para um projeto, que já fez um Pull-Request e foi aceito, mas não possui acesso ao colaborador. |
| Ator 03 | Sistema | O próprio GitHub em si |

## 3. Identificação dos Casos de Uso
| #UC   |      Nome UC      |  Descrição UC |
|--------|:----------------------:|:----------------:|
| UC-01 |  Abrir Pull-Request | Envio de commits de uma branch para outra com necessidade de verificações  |
| UC-02 |  Disparar e-mails | Envio de e-mails de alterações feitas no repositório  |
| UC-03 |  Requerer Review | Revisão de Pull Request por um segundo ator  |
| UC-04 |  Discutir Código | Comentar em Pull Request ou em Issues  |
| UC-05 |  Iniciar Integração Contínua | Verificação automatizada de código  |
| UC-06 |  Fechar Pull-Request | Insira aqui a descrição  |
| UC-07 |  Aceitar Pull-Request | Merge dos commits de um pull request aberto à branch destino  |
| UC-08 |  Utilizar Diff | Insira aqui a descrição  |
| UC-09 |  Revisar Código | Insira aqui a descrição  |
| UC-10 |  Comentar | Insira aqui a descrição  |

## 5. Diagrama de Caso de Uso

<a href="https://ibb.co/mrbYuQ"><img src="https://preview.ibb.co/fRX6EQ/use_case_diagram.png" alt="use_case_diagram" border="0"></a><br /><a target='_blank' href='https://imgbb.com/'> Diagrama de Caso de Uso </a><br />

## 6. Detalhamento dos Casos de Uso

### 1. UC-01 Abrir Pull-Request

**Atores**: Colaborador

**Pré-Condições**:
1. Colaborar deve estar logado em sua conta
1. Colaborador deve ter enviado commits para o GitHub
1. O projeto deve ter ao menos duas branchs

**Fluxo Princicpal**:
1. O colaborador entra no repositório do projeto e clica em "Pull Requests"
2. O colaborador seleciona a branch de destino das mudanças propostas
3. O colaborador preenche as informações de título e comentário do Pull Request.
4. O colaborador clica em "Create Pull Request"
5. O Pull Request é criado
6. O colaborador adiciona revisores ao Pull Request

**Fluxo Alternativo A**
1. Antes do passo 1 do **Fluxo Básico** se o colaborador acaba de enviar um commit para uma branch (a não ser a branch principal):
2. O sistema irá apresentar um botão "Open Pull Request"
3. O fluxo retorna para o passo 2 do fluxo básico

**Fluxo Alternativo B**
1. Antes do passo 1 do **Fluxo Básico** se o colaborador fez um fork do repositório e fez alterações no fora, ele pode solicitar a abertura de um Pull Request no repositório upstream
2. Colaborador acessa repositório fora
2. Colaborador clica em "New Pull Request"
3. O fluxo retorna para o passo 2 do fluxo básico

**Fluxo de Exceção A**
1. No passo 2 do **Fluxo Básico**  o colaborador pode receber um aviso de incompabilidade
2. O colaborador analisa o conflito 
3. O fluxo retorna para o passo 3 do fluxo básico

**Pós-condições**:
* **Pull Request criado**: O Pull Request é criado e passa ser listado na página de Pull Requests do repositório. E o colaborador pode adicionar revisores (contribuidores) para revisar as alterações feitas.

### 2. UC-02 Disparar e-mails

**Atores**: Colaborador, Sistema

**Pré-Condições**:
1. Colaborador deve estar logado em sua conta
1. Colaborador deve ter clicado no botão de *Watching*

**Fluxo Princicpal**:
1. O colaborador entra no repositório do projeto e clica em "Pull Requests"
2. O colaborador seleciona a branch de destino das mudanças propostas
3. O colaborador preenche as informações de título e comentário do Pull Request.
4. O colaborador clica em "Create Pull Request"
1. O colaborador assina um contribuidor a esse Pull Request
5. O Pull Request é criado
6. O sistema envia e-mail para o contribuidor

**Fluxo Alternativo A**
1. Antes do passo 1 do **Fluxo Básico** o colaborador clica em "Issues"
2. O colaborador assina um contribuidor a essa Issue
3. O fluxo retorna para o passo 6 do fluxo básico


**Pós-condições**:
* **E-mail enviado**: Um e-mail é enviado para o contribuidor e é indicado ao contribuidor na plataforma GitHub que há uma nova notificação.

### 3. UC-03 Requerer Review

**Atores**: Colaborador, Contribuidor

**Pré-Condições**:
1. Colaborar deve estar logado em sua conta
1. Colaborador deve ter enviado commits para o GitHub
1. O projeto deve ter ao menos duas branchs

**Fluxo Princicpal**:
1. O colaborador entra no repositório do projeto e clica em "Pull Requests"
2. O colaborador seleciona a branch de destino das mudanças propostas
3. O colaborador preenche as informações de título e comentário do Pull Request.
1. O colaborador clica em Reviewrs
1. Seleciona um contribuidor
4. O colaborador clica em "Create Pull Request"
5. O Pull Request é criado
6. O contribuidor é notificado que é um revisor

**Fluxo Alternativo A**
1. Antes do passo 1 do **Fluxo Básico** se o já houver um Pull Request aberto sem revisor:
2. Seleciona o Pull Request
3. O fluxo retorna para o passo 4 do fluxo básico


**Pós-condições**:
* **Revisor é adicionado ao Pull Request**: O Pull Request é criado com um revisor e será só merjado a branch de destino após a revisão.

### 3. UC-04 Comentar Código

**Atores**: Contribuidor

**Pré-Condições**:
1. Colaborar deve estar logado em sua conta
1. Colaborador deve ter enviado commits para o GitHub
1. O projeto deve ter ao menos duas branchs
1. Deve ter Pull Request aberto 

**Fluxo Princicpal**:
1. O cotribuidor entra no repositório do projeto e clica em "Pull Requests" 
1. Contribuidor seleciona um Pull Request aberto
1. Contribuidor clica no campo de comentário
1. Contribuidor inseri no campo o comentário 
1. Colaborador é notificado sobre o comentário


**Pós-condições**:
* **Adicionado comentário no Pull Request**: O Pull Request recebe um comentário e os envolvidos são notificados.

### 4. UC-04 Comentar Código

**Atores**: Contribuidor

**Pré-Condições**:
1. Colaborar deve estar logado em sua conta
1. Colaborador deve ter enviado commits para o GitHub
1. O projeto deve ter ao menos duas branchs
1. Deve ter Pull Request aberto 

**Fluxo Princicpal**:
1. O cotribuidor entra no repositório do projeto e clica em "Pull Requests" 
1. Contribuidor seleciona um Pull Request aberto
1. Contribuidor clica no campo de comentário
1. Contribuidor inseri no campo o comentário 
1. Colaborador é notificado sobre o comentário


**Pós-condições**:
* **Adicionado comentário no Pull Request**: O Pull Request recebe um comentário e os envolvidos são notificados.

### 5. UC-05 Iniciar Integração Contínua

**Atores**: Colaborador

**Pré-Condições**:
1. Colaborar deve estar logado em sua conta
1. Colaborador deve ter enviado commits para o GitHub
1. O projeto deve ter ao menos duas branchs
1. Configurar o aplicativo de terceiro no repositório

**Fluxo Princicpal**:
1. O colaborador entra no repositório do projeto e clica em "Pull Requests"
2. O colaborador seleciona a branch de destino das mudanças propostas
3. O colaborador preenche as informações de título e comentário do Pull Request.
4. O colaborador clica em "Create Pull Request"
5. O Pull Request é criado
6. A ferramenta analisa o Pull Request aberto
1. A ferramenta diz que o Pull Request está integro.

**Fluxo Alternativo A**
1. Após do passo 7 do **Fluxo Básico** se o Pull Request não estiver integro:
2. A ferramenta emitirá uma mensagem que esse Pull Request não deve ser aceito
3. O fluxo retorna para após passo 7 do fluxo básico

**Fluxo de Exceção A**
1. No passo 7 do **Fluxo Básico**  o colaborador pode receber um aviso de incompabilidade da ferramenta 
1. A ferramenta retorna uma mensagem de que não funciona com a linguagem em específica
3. O fluxo retorna para a passo 5 do fluxo básico sem checar o Pull Request

**Pós-condições**:
* **Pull Request é analisado**: O Pull Request é analisado e retornado a métrica que a ferramenta mediu.



### UC-07 Aceitar Pull-Request

#### Descrição
<p align="justify">
Este caso de uso é destinado ao usuário contribuidor que deseja aceitar um pull request aberto. Permite ao usuário contribuidor integrar realizar o merge dos commits contidos no pull request aberto à branch de destino, geralmente a branch principal do projeto.  
</p>

#### Atores
Contribuidor, Sistema.

#### Condições

##### _Pré-condições_
<p align="justify">
Caso o usuário contribuidor queira aceitar um pull request aberto, é necessário que o mesmo esteja logado no sistema e tenha as devidas permissões no repositório, além de existir um pull request aberto.
</p>

##### _Pós-condições_

Ao final desse caso de uso, os commits do pull request devem estar contidos na branch destino.

#### Fluxo de Eventos

#### Fluxo Principal
<p align="justify">
O fluxo principal inicia quando o usuário contribuidor clica no link _Pull requests_, que o redirecionará para a página de listagem de pull requests do projeto. 
</p>

1. O sistema lista os pull requests abertos, se houver. [FE01]
2. O contribuidor clica no _nome_ do pull request a ser aceito.
3. O sistema redireciona o contribuidor para a página de detalhamento do pull request aberto.
4. O sistema lista os commits contidos no pull request para o contribuidor. [FA01] [FA02]
5. O sistema indica ao contribuidor se existe conflitos ao comparar a branch origem com a branch destino.
6. O contribuidor clica no botão _Merge pull request_.
7. Os commits da branch origem são adicionados à branch destino.
8. O sistema cria um commit de merge.
9. O caso de uso é encerrado.

#### Fluxos Alternativos

##### [FA01] - Ver commits.
1. O contribuidor clica no link _Commits_, no menu da página de detalhamento do pull request aberto.
2. O sistema redireciona o contribuidor para a página de listagem dos commits do pull request aberto.
3. O sistema lista todos os commits contido no pull request aberto.

##### [FA02] - Visualizar commit específico.
1. O contribuidor clica em um dos commits listados.
2. O sistema redireciona o contribuidor para a página de visualização do commit selecionado.
3. O sistema mostra todas as adições, edições e/ou deleções daquele commit em comparação à branch destino.

#### Fluxo de Exceção

##### [FE01] - Campo em branco
<p aling="justify">
No episódio 1 do fluxo principal, não existe nenhum pull request aberto. O sistema retorna a mensagem "There aren’t any open pull requests.".
</p>