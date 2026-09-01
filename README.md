# 💠 Sistema de Clínica — Banco de Dados

## 📚 Sobre o projeto

Este projeto foi desenvolvido durante os estudos de **Banco de Dados**, com o objetivo de praticar a criação e organização de um banco de dados para o gerenciamento de uma **clínica médica**.

O projeto utiliza conceitos de **Modelagem de Banco de Dados**, incluindo a criação do **Modelo Entidade-Relacionamento (MER)**, do **Diagrama Entidade-Relacionamento (DER)**, além da elaboração de um **Dicionário de Dados** e arquivos **CSV com dados de teste**.

---

# 🎯 Objetivos do projeto

Durante o desenvolvimento deste projeto, foram praticados conceitos importantes relacionados à modelagem de bancos de dados:

* 🗂️ Modelagem de Banco de Dados;
* 🧩 Modelo Entidade-Relacionamento (MER);
* 📊 Diagrama Entidade-Relacionamento (DER);
* 🔑 Chaves primárias;
* 🔗 Relacionamentos entre entidades;
* 📖 Dicionário de Dados;
* 📄 Organização de dados em arquivos CSV;
* 🧪 Criação de dados para testes.

---

# 🛠️ Tecnologias e ferramentas utilizadas

| Tecnologia/Ferramenta | Utilização                              |
| --------------------- | --------------------------------------- |
| 🗄️ Banco de Dados    | Organização e modelagem das informações |
| 🧩 MER                | Representação conceitual das entidades  |
| 📊 DER                | Representação lógica do banco de dados  |
| 📄 CSV                | Armazenamento dos dados de teste        |
| 🐙 Git                | Versionamento do projeto                |
| 📂 GitHub             | Armazenamento e compartilhamento        |

---

# 📁 Estrutura do projeto

```text
📂 bd_mer_der_aula02
│
├── 📄 Clínica.CSV
├── 📄 Consulta.CSV
├── 📄 Médico.CSV
├── 📄 Paciente.CSV
│
├── 🖼️ MER_diagrama.png
├── 🖼️ DER_diagrama.png
│
├── 📊 MER_DER_excel.CSV
│
├── 📖 README.md
└── ⚙️ desktop.ini
```

---

# 🏥 Sistema da Clínica

O banco de dados foi desenvolvido para organizar informações relacionadas ao funcionamento de uma clínica.

As principais entidades presentes no sistema são:

* 👤 Paciente;
* 👨‍⚕️ Médico;
* 📅 Consulta;
* 🏥 Clínica.

Essas entidades permitem organizar e relacionar informações importantes do sistema.

---

# 🧩 Entidades do sistema

## 👤 Paciente

A entidade **Paciente** armazena as informações das pessoas cadastradas na clínica.

### Principais informações:

| Atributo   | Tipo    | Descrição                       |
| ---------- | ------- | ------------------------------- |
| `id`       | INT     | Identificador único do paciente |
| `nome`     | VARCHAR | Nome completo do paciente       |
| `RG`       | VARCHAR | Documento do paciente           |
| `idade`    | INT     | Idade do paciente               |
| `telefone` | VARCHAR | Telefone para contato           |
| `altura`   | DECIMAL | Altura do paciente              |
| `peso`     | DECIMAL | Peso do paciente                |

---

## 👨‍⚕️ Médico

A entidade **Médico** armazena as informações dos profissionais responsáveis pelos atendimentos.

### Principais informações:

| Atributo         | Tipo    | Descrição                        |
| ---------------- | ------- | -------------------------------- |
| `id`             | INT     | Identificador único do médico    |
| `nome`           | VARCHAR | Nome completo do médico          |
| `endereço`       | VARCHAR | Endereço relacionado ao cadastro |
| `especialização` | VARCHAR | Área de especialização           |

---

## 📅 Consulta

A entidade **Consulta** representa os atendimentos realizados ou agendados na clínica.

### Principais informações:

| Atributo      | Tipo    | Descrição                           |
| ------------- | ------- | ----------------------------------- |
| `id`          | INT     | Identificador único da consulta     |
| `data`        | DATE    | Data da consulta                    |
| `horario`     | TIME    | Horário da consulta                 |
| `sala`        | VARCHAR | Sala onde será realizada a consulta |
| `id_paciente` | INT     | Paciente relacionado à consulta     |
| `id_medico`   | INT     | Médico responsável pela consulta    |

---

# 🔗 Relacionamentos

O banco de dados possui relacionamentos entre as entidades.

## 👤 Paciente → 📅 Consulta

Um paciente pode possuir consultas cadastradas no sistema.

```text
PACIENTE
    │
    │ realiza
    ▼
CONSULTA
```

Cada consulta está relacionada a um paciente específico.

---

## 👨‍⚕️ Médico → 📅 Consulta

Um médico pode ser responsável por diversas consultas.

```text
MÉDICO
    │
    │ realiza
    ▼
CONSULTA
```

Cada consulta possui um médico responsável.

---

# 🧩 MER — Modelo Entidade-Relacionamento

O projeto possui um diagrama representando o **Modelo Entidade-Relacionamento (MER)**.

O MER é utilizado para representar a estrutura conceitual do banco de dados, identificando:

* Entidades;
* Atributos;
* Relacionamentos.

📄 Arquivo:

```text
MER_diagrama.png
```

---

# 📊 DER — Diagrama Entidade-Relacionamento

Também foi desenvolvido o **Diagrama Entidade-Relacionamento (DER)**.

O DER apresenta uma visão mais detalhada da estrutura do banco de dados e permite visualizar a organização das entidades e seus relacionamentos.

📄 Arquivo:

```text
DER_diagrama.png
```

---

# 📖 Dicionário de Dados

O projeto possui um arquivo contendo informações utilizadas como **Dicionário de Dados**.

Esse documento organiza os atributos das entidades e apresenta informações como:

* 🧩 Entidade;
* 📝 Nome do atributo;
* 🔤 Tipo de dado;
* 📏 Tamanho;
* 📖 Descrição.

📄 Arquivo:

```text
MER_DER_excel.CSV
```

---

# 🧪 Dados de teste

Foram criados arquivos CSV para representar dados que podem ser utilizados para testar a estrutura do banco de dados.

Os arquivos disponíveis são:

```text
📄 Paciente.CSV
📄 Médico.CSV
📄 Consulta.CSV
📄 Clínica.CSV
```

Esses dados podem ser utilizados futuramente para importar informações para um **Sistema Gerenciador de Banco de Dados (SGBD)**.

---

# 🔑 Conceitos praticados

## 🔑 Chave Primária

A chave primária é utilizada para identificar exclusivamente cada registro de uma entidade.

### Exemplo:

```text
Paciente
└── id
```

Cada paciente possui um identificador único.

---

## 🔗 Chave Estrangeira

As chaves estrangeiras permitem estabelecer relacionamentos entre diferentes tabelas.

### Exemplo:

```text
Consulta.id_paciente → Paciente.id
```

Isso permite identificar qual paciente está relacionado a uma consulta.

Outro relacionamento é:

```text
Consulta.id_medico → Médico.id
```

Assim, cada consulta pode ser associada ao médico responsável.

---

# 🧠 Principais aprendizados

Com o desenvolvimento deste projeto, foi possível praticar conhecimentos importantes relacionados a Banco de Dados:

* 🗄️ Modelagem de dados;
* 🧩 Criação de entidades;
* 📊 Desenvolvimento de MER e DER;
* 🔑 Identificação de chaves primárias;
* 🔗 Criação de relacionamentos;
* 📖 Documentação através do Dicionário de Dados;
* 📄 Organização de dados em CSV;
* 🧪 Criação de dados para testes;
* 🐙 Organização de projetos utilizando GitHub.

---

# 🚀 Possíveis melhorias futuras

Como evolução do projeto, podem ser implementadas funcionalidades como:

* 🗄️ Implementação do banco em MySQL;
* 📅 Sistema de agendamento de consultas;
* 👨‍⚕️ Cadastro de especialidades médicas;
* 📋 Histórico de consultas dos pacientes;
* 🏥 Melhor organização das informações da clínica;
* 💻 Desenvolvimento de uma aplicação para gerenciar os dados;
* 🌐 Criação de uma API integrada ao banco de dados;
* 📊 Criação de relatórios administrativos.

---

⭐ **Projeto desenvolvido para fins educacionais durante os estudos de Modelagem e Banco de Dados — 2026.**

# Projeto: Clinica - banco de dados

![MER DER Conceitual](./MER_diagrama.png)
![MER DER Lógico](./DER_diagrama.png)

## Dicionário de Dados

| Entidade      | Atributo         | Tipo    | Tamanho | Descrição                            |
| ------------- | ---------------- | ------- | ------- | ------------------------------------ |
| Paciente      | id               | INT     | -       | Identificador único do paciente      |
| Paciente      | nome             | VARCHAR | 100     | Nome completo do paciente            |
| Paciente      | RG               | VARCHAR | 14      | RG do paciente                       |
| Paciente      | idade            | INT     | -       | Idade de nascimento                  |
| Paciente      | telefone         | VARCHAR | 20      | Telefone do paciente                 |
| Paciente      | altura           | DECIMAL | 10,2    | Altura do paciente                   |
| Paciente      | peso             | DECIMAL | 10,2    | Peso do paciente                     |
| Médico        | id               | INT     | -       | Identificador único do médico        |
| Médico        | nome             | VARCHAR | 100     | Nome completo do médico              |
| Médico        | endereço         | VARCHAR | 20      | Endereço da consulta com o médico    |
| Médico        | especialização   | VARCHAR | 20      | Especialização do médico             |
| Consulta      | id               | INT     | -       | Identificador único da consulta      |
| Consulta      | data             | DATE    | -       | Data da consulta                     |
| Consulta      | horario          | TIME    | -       | Horário da consulta                  |
| Consulta      | sala             | VARCHAR | 30      | Sala da consulta                     |
| Consulta      | id_paciente      | INT     | -       | Paciente relacionado à consulta      |
| Consulta      | id_medico        | INT     | -       | Médico responsável pela consulta     |


## Dados de teste em CSV
- [Paciente.csv](./Paciente.CSV)
- [Médico.csv](./Médico.CSV)
- [Clínica.csv](./Clínica.CSV)
- [Consulta.csv](./Consulta.CSV)
