# Entrega 1 — Modelo Conceitual (DER)

### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

---

## Metadados

- **Alunos e RGM:**
  - Julia Otsubo — 47538317
  - Diogo Alves — 47236752
  - Karine Santos — 47430991
  - Matheus Guimarães — 49081144
  - Vinicius Agnoletto — 49604741

---

# 1. Caracterização da Organização

## Nome e natureza da organização

**E.K. Consultório Odontológico**

O E.K. Consultório Odontológico é um consultório odontológico de pequeno porte, voltado à realização de consultas e procedimentos odontológicos. A organização atua como pessoa física e é administrada diretamente pelas cirurgiãs-dentistas responsáveis.

## Contexto e porte

O consultório possui pequeno porte e conta com aproximadamente **3 cirurgiãs-dentistas** e **1 funcionária responsável pelo atendimento telefônico**.

As cirurgiãs-dentistas são responsáveis pela realização dos atendimentos, organização da agenda e demais atividades relacionadas ao funcionamento do consultório.

O volume de atendimento é de aproximadamente **5 a 9 pacientes por dia**, dependendo da agenda e da duração dos procedimentos realizados.

## Problemas e necessidades identificados

Durante o levantamento realizado na organização, foram identificadas necessidades relacionadas à organização e ao controle das informações do consultório.

Entre os principais pontos identificados estão:

- Organização dos agendamentos e horários das consultas;
- Controle dos dados dos pacientes;
- Organização dos prontuários e históricos dos pacientes;
- Registro e acompanhamento dos procedimentos realizados;
- Controle de pagamentos e possíveis pendências;
- Controle de materiais utilizados nos procedimentos;
- Controle do estoque de materiais;
- Organização dos cancelamentos e remarcações de consultas;
- Controle dos acessos às informações dos prontuários.

A proposta do sistema é centralizar essas informações, facilitando o gerenciamento das atividades e reduzindo a dependência de controles dispersos.

## Justificativa da escolha

A organização foi escolhida por ser um consultório real de pequeno porte ao qual o grupo possui acesso para levantamento de informações.

O consultório apresenta diferentes processos que envolvem geração, consulta e atualização de dados, como pacientes, consultas, profissionais, procedimentos, pagamentos, materiais e prontuários.

Dessa forma, apresenta quantidade e variedade de informações suficientes para a aplicação dos conceitos de modelagem de banco de dados estudados na disciplina.

## Evidências da organização

**Nome:** E.K. Consultório Odontológico

**Endereço:** Avenida Vital Brasil, nº 712 – Butantã – São Paulo/SP

**Telefone:** (11) 95311-4998

**E-mail:** consultorioodontoek@gmail.com

**Responsáveis:**
- Dra. Kátia Pinheiro
- Dra. Elielma Gomes

**Instagram:** @ek_odontologia

**WhatsApp:** 11953114998

[🔗 localização](https://www.google.com.br/maps/@-23.5704211,-46.7109521,729a,90y,354.68h,81.55t/data=!3m7!1e1!3m5!1sZQ7wLq3m06yJRXbGsnQGhA!2e0!6shttps:%2F%2Fstreetviewpixels-pa.googleapis.com%2Fv1%2Fthumbnail%3Fcb_client%3Dmaps_sv.tactile%26w%3D900%26h%3D600%26pitch%3D8.450000000000003%26panoid%3DZQ7wLq3m06yJRXbGsnQGhA%26yaw%3D354.68!7i16384!8i8192?hl=pt-BR&entry=ttu&g_ep=EgoyMDI2MDkyMS4wIKXMDSoASAFQAw%3D%3D)

As evidências da existência da organização e do acesso para levantamento de informações serão apresentadas por meio dos registros e materiais disponibilizados pelo grupo, respeitando a privacidade dos pacientes e demais envolvidos.

---

# 2. Processos de Negócio

## Principais processos mapeados

A partir do levantamento realizado no consultório, foram identificados os seguintes processos:

- Cadastro de pacientes;
- Agendamento de consultas;
- Cancelamento e remarcação de consultas;
- Realização de consultas;
- Registro de procedimentos;
- Atualização e consulta de prontuários;
- Controle de materiais utilizados nos procedimentos;
- Controle de estoque de materiais;
- Registro de pagamentos;
- Controle de acesso aos prontuários.

## Fluxograma

Foi elaborado um fluxograma para representar o processo de **cancelamento ou remarcação de consulta**.

O fluxo contempla a solicitação de alteração da consulta, consulta ao agendamento existente, decisão entre cancelamento ou remarcação, liberação do horário, registro do cancelamento ou busca por novo horário disponível.

O fluxograma encontra-se anexado separadamente ao repositório.

---

# 3. Requisitos do Sistema

## 3.1 Requisitos Funcionais

O sistema deverá ter os seguintes processos:

1. Cadastro dos pacientes

Para realizar essa função, é necessário:

- Nome completo
- Data de nascimento/idade
- CPF
- Telefone
- E-mail
- Endereço
- Número do paciente/ID
- Dados relevantes para identificação

2. Cadastro dos dentistas

Para realizar essa função, é necessário:

- Nome completo
- CPF
- CRO
- Telefone
- E-mail
- Especialidade
- Número do dentista/ID
- Dias e horários de atendimento

3. Visualizar a agenda dos dentistas

Para realizar essa função, é necessário:

- Identificação do dentista
- Data
- Horário
- Consultas agendadas
- Nome do paciente
- Status da consulta (agendada, cancelada, realizada etc.)
- Horários disponíveis

4. Agendar consultas

Para realizar essa função, é necessário:

- Paciente
- Dentista
- Data
- Horário
- Tipo/motivo da consulta
- Duração prevista
- Status da consulta
- Verificação da disponibilidade do dentista no horário escolhido

5. Cancelar consultas

Para realizar essa função, é necessário:

- Identificação da consulta
- Paciente
- Dentista
- Motivo do cancelamento, se necessário
- Alteração do status para “cancelada”
- Liberação do horário na agenda

6. Remarcar consultas

Para realizar essa função, é necessário:

- Identificação da consulta atual
- Paciente
- Dentista
- Novo dia
- Novo horário
- Verificação da disponibilidade
- Registro da alteração
- Liberação do horário anterior

7. Dentista acessar os dados dos pacientes

Para realizar essa função, é necessário:

- Login do dentista
- Senha
- Identificação do profissional
- Permissão de acesso
- Cadastro do paciente
- Dados pessoais e clínicos autorizados

8. Registrar consultas realizadas

Para realizar essa função, é necessário:

- Paciente
- Dentista
- Data
- Horário
- Motivo da consulta
- Observações do dentista
- Diagnóstico, quando aplicável
- Status como “realizada”

9. Registrar procedimentos odontológicos realizados

Para realizar essa função, é necessário:

- Paciente
- Consulta relacionada
- Dentista responsável
- Nome do procedimento
- Data
- Descrição/observações
- Valor, quando aplicável

10. Consultar histórico de consultas dos pacientes

Para realizar essa função, é necessário:

- Identificação do paciente
- Consultas anteriores
- Data
- Dentista
- Motivo/tipo da consulta
- Status
- Observações ou informações registradas

11. Consultar histórico de procedimentos odontológicos dos pacientes

Para realizar essa função, é necessário:

- Identificação do paciente
- Procedimentos realizados
- Data
- Dentista responsável
- Consulta relacionada
- Nome do procedimento
- Observações
- Valor, se houver

12. Registrar pagamentos realizados e pendentes

Para realizar essa função, é necessário:

- Paciente
- Consulta/procedimento relacionado
- Valor
- Data de pagamento
- Forma de pagamento
- Status: pago ou pendente
- Identificação do pagamento

13. Emitir recibos e comprovantes de pagamento

Para realizar essa função, é necessário:

- Identificação do paciente
- Consulta/procedimento
- Valor pago
- Data do pagamento
- Forma de pagamento
- Número/identificação do pagamento
- Geração do recibo/comprovante
-

## 3.2 Requisitos Não Funcionais

O sistema deverá apresentar:

- **Segurança:** as informações dos pacientes e dos prontuários devem ser protegidas contra acessos não autorizados;
- **Controle de acesso:** cada usuário deverá possuir identificação e perfil de acesso;
- **Usabilidade:** a interface deverá ser simples e facilitar a utilização pelos funcionários e profissionais do consultório;
- **Desempenho:** o sistema deverá permitir consultas e registros das informações de forma eficiente;
- **Disponibilidade:** as informações deverão estar disponíveis aos usuários autorizados durante o funcionamento do consultório;
- **Integridade:** os dados registrados deverão permanecer consistentes e organizados;
- **Privacidade:** informações pessoais e clínicas deverão ser tratadas de forma restrita e adequada.

---

# 4. Regras de Negócio

## Regras operacionais

- Um paciente pode possuir um prontuário.
- Um paciente pode possuir várias consultas.
- Uma consulta deve estar relacionada a um paciente.
- Uma consulta deve estar relacionada a um dentista responsável.
- Um dentista pode realizar várias consultas.
- Uma consulta pode possuir vários procedimentos.
- Um procedimento pode possuir registros de pagamento.
- Um procedimento pode utilizar materiais.
- Um material pode ser utilizado em diferentes procedimentos.
- A utilização de materiais deve registrar a quantidade utilizada e a data de utilização.
- Um prontuário pode possuir diversos registros de acesso.
- Um usuário pode realizar diversos acessos aos prontuários.
- O acesso às informações do prontuário deve ser realizado por usuário identificado.
- O cancelamento de uma consulta deve liberar o horário anteriormente reservado.
- A remarcação de uma consulta depende da existência de um novo horário disponível.

## Restrições organizacionais

- Os dados dos pacientes devem ser tratados de forma restrita, devido à natureza das informações armazenadas.
- O acesso aos prontuários deve ser limitado aos usuários autorizados.
- As informações registradas no sistema devem permanecer organizadas e consistentes.
- O sistema deve permitir o acompanhamento das informações relacionadas a consultas, procedimentos, pagamentos e materiais.

---

# 5. Dicionário de Dados Conceitual (Preliminar)

O dicionário de dados foi elaborado a partir das entidades, atributos e regras identificadas durante a modelagem conceitual.

O documento apresenta, para cada entidade, seus respectivos atributos, suas descrições e as regras de negócio associadas.

As entidades utilizadas no modelo são:

- PACIENTE;
- PRONTUARIO;
- DENTISTA;
- CONSULTA;
- PROCEDIMENTO;
- PAGAMENTO;
- MATERIAL;
- PROCEDIMENTO_MATERIAL;
- ESPECIALIDADE;

O **Dicionário de Dados em HTML** está anexado separadamente ao repositório.

---

# 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

## Entidades reconhecidas

### PACIENTE

Representa as pessoas atendidas pelo consultório.

**Atributos:**
- ID_Paciente;
- Nome;
- CPF;
- Data_Nascimento;
- Telefone;
- E-mail.

### PRONTUARIO

Representa o registro das informações relacionadas ao histórico e acompanhamento do paciente.

**Atributos:**
- ID_Prontuario;
- Data_Atualizacao;
- Historico;
- Observacoes.

### DENTISTA

Representa os profissionais responsáveis pelos atendimentos odontológicos.

**Atributos:**
- ID_Dentista;
- Nome;
- CRO;
- Especialidade.

### CONSULTA

Representa os agendamentos e atendimentos realizados pelos dentistas.

**Atributos:**
- ID_Consulta;
- Data;
- Horario;
- Status.

### PROCEDIMENTO

Representa os procedimentos odontológicos realizados durante as consultas.

**Atributos:**
- ID_Procedimento;
- Nome;
- Descricao;
- Valor.

### PAGAMENTO

Representa os registros de pagamento relacionados aos procedimentos.

**Atributos:**
- ID_Pagamento;
- Data_Pagamento;
- Valor;
- Forma_Pagamento;
- Status.

### MATERIAL

Representa os materiais disponíveis e controlados pelo consultório.

**Atributos:**
- ID_Material;
- Nome;
- Quantidade;
- Unidade;
- Data_Validade;
- Estoque_Minimo.

### PROCEDIMENTO_MATERIAL

Representa o registro da utilização de materiais durante os procedimentos.

**Atributos:**
- ID_Utilizacao;
- Quantidade_Utilizada;
- Data_Utilizacao.

### ESPECIALIDADE

Representa a área de atuação odontológica da(o) dentista.

**Atributos:**
- ID_Especialidade;
- Nome_especialidade;
- Descrição;

## Relacionamentos pertinentes

- **PACIENTE — POSSUI — PRONTUARIO:** um paciente possui um prontuário e um prontuário pertence a um paciente.
- **PACIENTE — POSSUI — CONSULTA:** um paciente pode possuir várias consultas.
- **DENTISTA — REALIZA — CONSULTA:** um dentista pode realizar várias consultas.
- **CONSULTA — POSSUI — PROCEDIMENTO:** uma consulta pode possuir vários procedimentos.
- **PROCEDIMENTO — POSSUI — PAGAMENTO:** um procedimento pode possuir registros de pagamento.
- **PROCEDIMENTO — UTILIZA — PROCEDIMENTO_MATERIAL:** um procedimento pode utilizar vários registros de materiais.
- **MATERIAL — PARTICIPA DE — PROCEDIMENTO_MATERIAL:** um material pode participar de vários registros de utilização.
- **DENTISTA - POSSUI - ESPECIALIDADE:** uma especialidade pode estar associada a vários dentistas

## Restrições e políticas organizacionais aplicadas ao modelo

O modelo considera a necessidade de controle e proteção das informações dos pacientes, principalmente em relação aos prontuários.

Também considera a necessidade de organização dos agendamentos, procedimentos, pagamentos e materiais, além do registro dos usuários que acessam os prontuários.

---

# 7. Diagrama Entidade-Relacionamento (DER)

O Diagrama Entidade-Relacionamento Conceitual foi desenvolvido para representar graficamente as entidades, atributos, relacionamentos e cardinalidades identificados durante o levantamento e a modelagem.

O DER contém as seguintes entidades:

- PACIENTE;
- PRONTUARIO;
- DENTISTA;
- CONSULTA;
- PROCEDIMENTO;
- PAGAMENTO;
- MATERIAL;
- PROCEDIMENTO_MATERIAL;
- ESPECIALIDADE;

O diagrama está anexado separadamente ao repositório em formato de imagem.

---

# 8. Justificativa Técnica

A modelagem foi estruturada considerando os principais dados e processos identificados no consultório odontológico.

A entidade **PACIENTE** foi definida para centralizar as informações cadastrais das pessoas atendidas. O **PRONTUARIO** foi separado para representar as informações relacionadas ao histórico e acompanhamento do paciente.

A entidade **CONSULTA** foi criada para representar os agendamentos e atendimentos, permitindo relacioná-los tanto aos pacientes quanto aos dentistas responsáveis.

A entidade **PROCEDIMENTO** foi separada de CONSULTA para representar os diferentes procedimentos que podem ocorrer durante uma consulta. Essa separação também permite relacionar os procedimentos aos respectivos pagamentos e aos materiais utilizados.

A entidade **PROCEDIMENTO_MATERIAL** foi utilizada como entidade associativa para representar a utilização de materiais nos procedimentos, permitindo registrar informações específicas dessa utilização, como quantidade e data.

As cardinalidades foram definidas de acordo com a lógica dos processos representados no modelo e com a necessidade de permitir que a estrutura possa ser expandida nas próximas etapas do projeto.

---

# 9. Uso de Inteligência Artificial

O grupo utilizou a ferramenta **ChatGPT** durante diferentes etapas do desenvolvimento do trabalho.

## Ferramenta e etapa

**Ferramenta:** ChatGPT

A ferramenta foi utilizada nas seguintes etapas:

- Organização das informações levantadas;
- Estruturação do README;
- Organização dos requisitos funcionais e não funcionais;
- Identificação e organização de regras de negócio;
- Apoio na definição das entidades, atributos e relacionamentos;
- Criação e revisão do DER;
- Criação do fluxograma;
- Identificação e correção de algumas lacunas e inconsistências encontradas durante a modelagem;
- Revisão e organização textual do trabalho.

## Motivação

A IA foi utilizada como ferramenta de apoio para organizar as informações obtidas pelo grupo, auxiliar na estruturação da documentação e identificar possíveis inconsistências na modelagem.

As sugestões fornecidas pela IA foram analisadas pelo grupo e comparadas com as informações obtidas durante o levantamento da organização.

## Prompts utilizados

Entre os prompts utilizados, estão solicitações relacionadas a:

- Organização das informações da organização no modelo fornecido pelo professor;
- Identificação de entidades, atributos e relacionamentos para o sistema;
- Estruturação dos requisitos funcionais e não funcionais;
- Criação e revisão das regras de negócio;
- Criação de fluxogramas dos processos identificados;
- Criação e correção do Diagrama Entidade-Relacionamento;
- Identificação de erros técnicos, cardinalidades incorretas e lacunas no modelo.

## Resposta recebida

A IA auxiliou o grupo na organização da estrutura do trabalho, sugerindo formas de representar os processos, requisitos, regras de negócio, entidades, atributos, relacionamentos e cardinalidades.

Também foram identificadas inconsistências em versões preliminares do DER e realizados ajustes na estrutura do diagrama, incluindo a organização das entidades relacionadas a prontuários, acessos, procedimentos, pagamentos e utilização de materiais.

## Fontes consultadas e verificadas

As informações específicas sobre o funcionamento do consultório foram obtidas por meio do levantamento realizado pelo grupo na própria organização.

As sugestões fornecidas pela IA não foram consideradas como substitutas das informações obtidas durante a pesquisa de campo.

## Trechos rejeitados ou corrigidos

Algumas sugestões e versões geradas pela IA foram corrigidas ou descartadas quando apresentavam inconsistências com as informações levantadas ou com a estrutura exigida para um modelo conceitual.

Também foram corrigidos erros identificados em versões preliminares do DER, especialmente relacionados a relacionamentos, cardinalidades e posicionamento de entidades.

## Justificativa da escolha final

As decisões finais foram tomadas pelo grupo com base nas informações levantadas sobre o consultório e nos requisitos apresentados para a atividade.

A IA foi utilizada como ferramenta de apoio, enquanto a validação e decisão sobre o conteúdo final permaneceram sob responsabilidade dos integrantes do grupo.

## Reflexão crítica

O uso da IA facilitou a organização das informações e ajudou na identificação de possíveis erros de modelagem. Entretanto, também foram observadas limitações, principalmente na geração automática de diagramas, que apresentou inconsistências em algumas versões.

Por esse motivo, as respostas da IA foram revisadas pelo grupo e comparadas com as informações levantadas na organização. A ferramenta foi utilizada como apoio à construção do trabalho, e não como fonte única de informação ou validação do modelo.

---

# Arquivos da Entrega

- `README.md` — documentação principal do projeto;
- `DER` — Diagrama Entidade-Relacionamento Conceitual em imagem;
- `Dicionario_de_Dados.html` — Dicionário de Dados Conceitual;
- `Fluxograma_Cancelamento_Remarcacao.png` — fluxograma do processo de cancelamento ou remarcação de consulta.
- `avaliacao_participação_grupo.pdf` - autoavaliação do grupo
