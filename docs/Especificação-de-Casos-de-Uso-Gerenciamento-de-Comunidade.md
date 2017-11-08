# DOCUMENTO DE CASOS DE USOS 
## Tema: Gerenciamento de Comunidade | Grupo: GitHub
### Aluno responsável: Weyler Almeida Gomes


## 1. Introdução
Através de uma análise profunda da equipe, foi decidido "dividir" o GitHub em funcionalidades principais (onde o próprio GitHub define essas funcionalidades principais) e cada integrante(es) da equipe ficou responsável em elaborar o Diagrama de Casos de Uso e a Especificação de Casos de Uso. Logo a funcionalidade Gerenciamento de Comunidade ficou de responsabilidade do aluno Weyler Almeida.

## 2. Identificação dos atores
| Ator   |      Nome do Ator      |  Descrição Ator |
|--------|:----------------------:|:----------------:|
| Ator 01 | Usuário | Pessoa comum que tenha acesso ao site. |
| Ator 02 |  Colaborador | Uma pessoa que está envolvida em uma organização e que possa ler, escrever ou possuir permissões de administrador para um ou mais repositórios na sua organização.  |
| Ator 03 | Membro | Usuário que possui permissões reduzidas com relação ao colaborador de uma organização. Sendo membro uma especialização de Colaborador. |
| Ator 04 | Sistema | O próprio GitHub em si. |

## 3. Identificação dos Casos de Uso
| #UC   |      Nome UC      |
|--------|:----------------------:|
| UC-01 |  Criar organização |
| UC-02 |  Convidar membros para a organização |
| UC-03 |  Remover membros da organização  |
| UC-04 |  Mudar permissão de membros  |
| UC-05 |  Criar time |
| UC-06 |  Renomear time |
| UC-07 |  Remover time |
| UC-08 |  Mudar visibilidade do time |

## 5. Diagrama de Caso de Uso

![gerenciamento de comunidade](https://user-images.githubusercontent.com/21064965/32178249-68ddfee6-bd73-11e7-951f-5d2ac1822aa6.png)

## 6. Detalhamento dos Casos de Uso

### 1. UC-01 Criar Organização

#### Atores:
Usuário, Sistema

#### Pré-Condições:
1. O usuário deve estar logado em sua conta.

#### Fluxo Principal:

1. Usuário abre a aba de seu perfil e entra em configurações.
2. Usuário acessa a parte de organizações e clica em “New organization”.
3. Usuário adiciona o nome e o e-mail da organização. – FE1 e FE2
4. Usuário escolhe o plano de pagamento. – FA2
5. Usuário escolhe se a organização pertence a uma empresa. – FA3
6. Sistema habilita o botão de confirmação.
7. Usuário confirma a criação da organização.
8. Sistema leva o usuário até a página principal de sua organização.
9. Usuário torna-se colaborador da organização.

#### Fluxo Alternativo:

##### [FA01] - Acesso alternativo à página de criação da organização

1. Usuário acessa a barra de rolagem com o seu nome na página principal de seu perfil.
2. Usuário clica em “Create organization”.
3. Caso de uso retorna ao FP3.


##### [FA02] - Planos não gratuitos de pagamento

1. Usuário escolhe entre o plano TEAM e o plano BUSINESS.
2. Sistema acrescenta campos de informações que o usuário deve preencher.
3. Usuário entra com o número de usuários máximo na organização.
4. Sistema adequa o valor mensal do plano com relação ao valor digitado pelo usuário.
5. Usuário informa os dados do cartão ou efetua o pagamento pelo serviço PayPal. – FE3
6. Caso de uso retorna ao FP5.

##### [FA03] - Organização pertence a uma empresa

1. Usuário seleciona a opção em que a organização pertence a uma empresa.
2. Sistema acrescenta um campo para a inserção do nome da empresa.
3. Usuário insere o nome da empresa.
4. Caso retorna ao FP6.

#### Fluxo de Exceção:

##### [FE01] - Nome da organização inválido

1. Usuário digita um nome já utilizado por outra organização.
2. Sistema notifica o usuário com uma mensagem de erro.
3. Sistema aguarda alteração do nome.

##### [FE02] - E-mail inválido

1. Usuário insere um e-mail inválido na página de criação da organização.
2. Sistema notifica o usuário com uma mensagem de erro.
3. Sistema aguarda alteração do e-mail.

##### [FE03] - Erro no processo de pagamento

1. Usuário insere informações inválidas na sessão de pagamento.
2. Usuário confirma a criação da organização.
3. Sistema retorna à página de criação.
4. Sistema notifica o usuário com uma mensagem de erro.


#### Pós-condições:
##### Organização criada:
A organização é criada e passa a ser listada na página de organizações do perfil do usuário. O usuário pode adicionar/remover membros, mudar permissões de membros, criar times, etc.


### UC-02 Convidar membros da organização

#### Atores:
Colaborador, Sistema.

#### Pré-condições:
<p align="justify">
O colaborador deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Colaborador clica em sua foto de perfil e em “Your Profile”.
2. Colaborador seleciona usa organização.
3. Colaborador seleciona a aba “People” e clica em “Invite member”.
4. Colaborador insere o nome ou o e-mail da pessoa que se quer convidar. – FE1
5. Colaborador escolhe os privilégios da pessoa na organização.
6. Colaborador confirma o envio do convite.


#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### [FE01] - Usuário não encontrado

1. Colaborador insere o nome/e-mail de usuário não cadastrado no sistema.
2. Sistema notifica o usuário com uma mensagem de aviso.
3. Sistema aguarda a alteração.

#### Pós-condições:
##### Convite enviado:
Após a finalização do caso de uso, um e-mail é enviado para o usuário que está sendo convidado.

### UC-03 Remover membros da organização

#### Atores:
Colaborador.

#### Pré-condições:
<p align="justify">
O colaborador deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Colaborador clica em sua foto de perfil e em “Your Profile”.
2. Colaborador seleciona sua organização.
3. Colaborador seleciona a aba “People”.
4. Colaborador seleciona os membros no qual deseja remover.
5. Colaborador seleciona “Remove from organization” no menu de rolagem em cima da lista de usuários.
6. Colaborador confirma a remoção.

#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### Não se aplica

#### Pós-condições:

##### Membro removido:
Após a finalização do caso de uso, o(s) membros selecionado(s) é(são) removido(s) da organização.


### UC-04 Mudar permissão de membros

#### Atores:
Colaborador.

#### Pré-condições:
<p align="justify">
O colaborador deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Colaborador clica em sua foto de perfil e em “Your Profile”.
2. Colaborador seleciona sua organização.
3. Colaborador seleciona a aba “People”.
4. Colaborador seleciona um ou mais membros para promover.
5. Colaborador clica em “Change role” no menu de rolagem em cima da lista de membros.
6. Colaborador seleciona qual papel os membros devem exercer e confirma a alteração.

#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### Não se aplica

#### Pós-condições:

##### Permissão de membro mudada:
Após a finalização do caso de uso, o(s) membros selecionado(s) é(são) promovidos\rebaixados para a permissão selecionada pelo colaborador.


### UC-05 Criar time

#### Atores:
Membro.

#### Pré-condições:
<p align="justify">
O membro deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Membro clica em sua foto de perfil e em “Your profile”.
2. Membro seleciona sua organização.
3. Membro acessa a aba “Teams” e clica em “New team”.
4. Membro insere o nome do time, a descrição (opcional) e o time pai.
5. Membro escolhe a visibilidade do time.
6. Membro confirma a criação do time.

#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### Não se aplica

#### Pós-condições:

##### Time criado:
Após a finalização do caso de uso, o time é criado tendo como “presidente” do time o membro que o criou.

### UC-06 Renomear time

#### Atores:
Colaborador ou membro que tenha criado o time.

#### Pré-condições:
<p align="justify">
O colaborador/membro deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Membro clica em sua foto de perfil e em “Your profile”.
2. Membro seleciona sua organização.
3. Membro acessa a aba “Teams” e seleciona o time que se deseja renomear.
4. Membro acessa a parte de configuração.
5. Membro altera o nome do time.
6. Membro confirma a alteração.

#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### Não se aplica

#### Pós-condições:

##### Time renomeado:
Após a finalização do caso de uso, o time é renomeado.

### UC-07 Remover time

#### Atores:
Colaborador ou membro que tenha criado o time.

#### Pré-condições:
<p align="justify">
O colaborador/membro deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Membro clica em sua foto de perfil e em “Your profile”.
2. Membro seleciona sua organização.
3. Membro acessa a aba “Teams” e seleciona o(s) time(s) que se deseja excluir.
4. Membro seleciona “Delete” no menu de rolagem acima da lista de times.
5. Membro confirma a exclusão do time.

#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### Não se aplica

#### Pós-condições:

##### Time excluído:
Após a finalização do caso de uso, o time é removido.

### UC-08 Mudar visibilidade do time

#### Atores:
Colaborador ou membro que tenha criado o time.

#### Pré-condições:
<p align="justify">
O colaborador/membro deve estar logado em sua conta.
</p>

#### Fluxo Principal:

1. Membro clica em sua foto de perfil e em “Your profile”.
2. Membro seleciona sua organização.
3. Membro acessa a aba “Teams” e seleciona o(s) time(s) que se deseja alterar a visibilidade.
4. Membro seleciona “Change visibility” no menu de rolagem acima da lista de times.
5. Membro escolhe o time de visibilidade do time e confirma a alteração.

#### Fluxos Alternativos

##### Não se aplica

#### Fluxo de Exceção

##### Não se aplica

#### Pós-condições:

##### Visibilidade do time alterada:
Após a finalização do caso de uso, a visibilidade do time é alterada.