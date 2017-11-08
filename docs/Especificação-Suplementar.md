## 1. Introdução
Este documento captura os requisitos de sistema que não foram identificados imediatamente nos Casos de Uso do Modelo de Casos de Uso. Entre estes requisitos estão incluídos:

* Atributos de qualidade do sistema a ser criado, incluindo requisitos de usabilidade,confiabilidade, desempenho e suportabilidade.
* Outros requisitos, como sistemas operacionais e ambientes, requisitos de compatibilidade e restrições de design. 

### 1.1 Finalidade
A finalidade deste documento é definir os requisitos do sistema do GitHub. Esta especificação suplementar lista os requisitos que não são imediatamente capturados nos casos de uso no modelo de casos de uso. As especificações es e o modelo de casos de uso, juntos, capturam um conjunto completo de requisitos do sistema.

### 1.2 Escopo 
O objetivo do GitHub é tornar prático e rápido o versionamento de código, tanto para usuários comuns como para corporações.

### 1.3 Definições, Acrônimos e Abreviações
Não utilizado atualmente

### 1.4 Referências
* Entrevistas    
* Questionários    
* Artigos externos    
* Diagramas de caso de usos    
* Cenários    
* Léxicos    

### 1.5 Visão Geral
Este documento apresenta, inicialmente, uma introdução ao projeto para ambientação com o problema. A seguir, são expostos os requisitos suplementares distribuídos em funcionalidade, usabilidade, confiabilidade, desempenho, suportabilidade, restrições de design, requisitos de sistemas de ajuda e de documentação de usuário on-line, interfaces, requisitos de licenciamento, observações legais de Copyright e outras e padrões aplicáveis.

## 2. Funcionalidade
Os requisitos funcionais são capturados através dos casos de uso definidos.

<!-- ### 2.1 Requisitos Não-Funcionais -->

## 3. Usabilidade
* Facilidade de uso.
* A interface de usuário ser desenvolvida levando em consideração as melhores práticas sobre UI/UX.
* A interface de usuário deve ser responsiva e adaptável a dispositivos móveis.
* A interface de usuário em dispositivos móveis deve conter apenas funcionalidades que não necessitem de muita interação do desenvolvedor.
* A interface de usuário deve 
* A plataforma exigirá do usuário que ele saiba utilizar um navegador da Web, bem como tenha conhecimento básico dos conceitos e usos da ferramenta de versionamento GIT.

## 4. Confiabilidade
### 4.1 Segurança Física
* Acesso aos data center limitados aos técnicos e aprovados pelo staff do Github
* Leitura de biometria para controlar o acesso aos data centers
* Câmeras de seguranças monitorando todas as localizações dos datas centers 
* 24/7 fornecimento de proteção adicional contra a entrada não autorizada
* Segurança física auditada por uma empresa independente

### 4.2 Segurança de Sistemas
* Firewall dedicado e serviços VPN para ajudar a bloquear o acesso não autorizado ao sistema.
* Serviços de mitigação de serviços de denegação distribuída (DDoS) alimentados por soluções líderes do setor.

### 4.3 Segurança Operacional
* Elaboração de registros e rastreio de acessos para fins de auditoria.
* Elaboração políticas documentadas para destruição de informações sensitivas.
* Elaboração de documentos para mudança em procedimentos de gerenciamento.
* Submissão do data center primário de operações a agência independentes para processos de auditoria.

### 4.4 Segurança de Software
O GitHub emprega uma equipa de especialistas em servidores 24 horas por dia, 7 dias por semana por 365 dias ao ano. Para manter o software e suas dependências atualizadas, eliminando potenciais vulnerabilidades de segurança. Utiliza-se uma ampla gama de soluções de monitoramento para prevenir  e eliminar ataques ao site.

### 4.5 Comunicações
* Toda a troca de dados com a plataforma deverá ser transmitida via SSL.
* Troca de dados relacionados a push e pull de dados privados deverá ser feita via SSH, autenticada com chaves privadas, ou via HTTPS usando os dados de nome de usuário e senha do desenvolvedor.
* Credenciais de login SSH usados para push e pull não devem ser utilizada para acesso shell ou o sistema de arquivos. 

### 4.6 Sistema de Arquivos e backups

Cada peça de hardware que usa-se tem uma cópia idêntica pronta e aguardando um hot-swap imediato em caso de falha de hardware ou software. Toda linha de código que armazena-se é guardada em no mínimo três servidores diferentes, incluindo um backup fora do local. Não remove-se retroativamente os repositórios de backups quando excluídos pelo usuários, pois talvez deve-se restaurar o repositório para o usuário se ele for removido acidentalmente.

O GitHub não criptografa os repositórios no disco porque não seria mais seguro: o site e o backend git precisam decifrar os repositórios sob demanda, diminuindo o tempo de resposta. Qualquer usuário com acesso de shell ao sistema de arquivos teria acesso a rotina de descriptografia, negando assim qualquer segurança que ele forneça. Portanto, nos concentramos em tornar nossas máquinas e redes tão seguras quanto possível.

### 4.7 Acesso de empregados
* Nenhum empregado deve ter acesso a repositórios privados, exceto em casos necessários como prestação de suporte técnico.

### 4.8 Manutenção da segurança
Protege-se seu login de ataques de força bruta com limitação de taxa. Todas as senhas são filtradas de todos os registros e são de um jeito criptografadas no banco de dados usando o bcrypt. As informações de login são sempre enviadas por SSL.

Permite-se que você use a autenticação de dois fatores, ou 2FA, como uma medida de segurança adicional ao acessar sua conta do GitHub. A ativação do 2FA adiciona segurança à sua conta exigindo tanto sua senha como o acesso a um código de segurança no seu telefone para acessar sua conta.

Há um pessoal de segurança em tempo integral para ajudar a identificar e prevenir novos vetores de ataque. Sempre há teste novos recursos para excluir potenciais ataques, como wikis protegendo o XSS e garantindo que as Páginas não possam acessar os cookies.

Também mantém relacionamentos com empresas de segurança respeitáveis ​​para realizar testes de penetração regulares e auditorias contínuas do GitHub e seu código.

Para empresas, oferecemos o GitHub Enterprise, uma versão do GitHub que pode ser instalada em um servidor dentro da rede da empresa.

### 4.9 Segurança de cartão de crédito
As informações de cartão de créditos, utilizadas para fazer upgrade de contas não deverão ser guardadas nos servidores.


## 5. Desempenho
* Tempo de resposta: O sistema deve responder à uma requisição do usuário em no máximo 3 segundos
* Tempo de carregamento da página: A aplicação deve ser carregada em no máximo 3 segundos, para conexões mais lentas, e de 1 segundo, para conexões mais rápidas;
* O software é capaz de atender acessos simultâneos de diferentes usuários.

## 6. Suportabilidade
* A plataforma deverá ser carregada em todos os navegadores, por exemplo: Google Chrome, Internet Explorer, Mozilla Firefox e Safari.

## 7. Restrições de Design
O design do sistema da plataforma deverá estar em conformidade com os padrões de tecnologia web em uso atualmente, tais como o padrão HTML e JavaScript, Ruby on Rails, etc.

## 8. Requisitos de Sistema de Ajuda e de Documentação de Usuário On-line
A plataforma conterá um guia para auxiliar a utilização de funcionalidades elementares como : criar repositórios e branch,  fazer e comitar mudanças, abrir um Pull Request e fazer merge. Além disso conterá o GitHub Help que irá contemplar um guia para todas as funcionalidades em exercício da plataforma.

## 9. Interfaces 
### 9.1 Interfaces de Usuário
* Interface de Login : Caso o usuário já tenha se cadastrado no github, essa tela o permite acessar as demais aplicações disponibilizadas na plataforma, via seu login. Caso contrário, terá a opção de se cadastrar no github.
* Interface de Cadastramento : Permite o cadastro de um novo usuário;
* Interface de Recuperação de Senha : Permite ao usuário já cadastrado mandar um email requerendo uma nova senha.
* Tela Inicial : Visualização dos repositórios em que o usuário contribuiu e os seus próprios repositórios.
* Tela Inicial da Organização : Visualização de todos os repositórios referentes à organização.

### 9.2 Interfaces de Hardware
* Smartphone, tablets, desktop. 

### 9.3 Interfaces de Software
* Sistema de controle de versão Git.

### 9.4 Interfaces de Comunicação
* Wi-fi
* Rede móvel

## 10. Requisitos de Licenciamento
A utilização do software é garantida a qualquer usuário.