# Dashboard de Indicadores de Assistência Social

[🔗 Acessar o dashboard no Power BI](https://app.powerbi.com/groups/me/reports/5fd6b942-3086-4645-ab69-99d2ea93ab22?ctid=53b7d7a8-f263-42f4-8ced-11a95d2f5a38&pbi_source=linkShare&bookmarkGuid=0f9c4075-c56a-4a09-aa18-193d8def1afd)

## Sobre o projeto

Este projeto consiste em um dashboard desenvolvido para facilitar o acesso e a análise dos indicadores de atendimento dos serviços de assistência social da prefeitura onde atuo.

O relatório foi desenvolvido no **Power BI**, utilizando técnicas de tratamento, modelagem e análise de dados para consolidar informações provenientes de diferentes bases e apresentar os principais indicadores de forma visual e interativa.

> **Importante:** para fins de portfólio e preservação de informações institucionais, todos os dados disponibilizados neste repositório são **fictícios** e foram gerados artificialmente utilizando a temática do universo de *Harry Potter*. Os dados apresentados não representam informações reais da prefeitura, de seus usuários ou dos serviços de assistência social.

## Tecnologias e ferramentas

* **Power BI**
* **Power Query / Linguagem M**
* **DAX**
* **Modelagem dimensional**
* **Modelo estrela**
* **SQL / conceitos de banco de dados**

## Objetivo

O principal objetivo do projeto foi criar uma ferramenta que permitisse consultar e analisar rapidamente informações relacionadas aos atendimentos realizados pelos serviços de assistência social.

A solução foi estruturada para permitir análises por diferentes perspectivas, como:

* Perfil demográfico dos usuários;
* Distribuição de renda;
* Quantidade de atendimentos;
* Evolução dos atendimentos ao longo do tempo;
* Distribuição territorial;
* Unidades responsáveis pelos atendimentos;
* Características dos públicos atendidos.

## Metodologia

### 1. Bases de dados

Para a construção do modelo, foram consideradas três fontes principais de informação:

* **Cadastro Único** — informações cadastrais e socioeconômicas;
* **Benefício de Prestação Continuada (BPC)** — informações relacionadas ao benefício;
* **IRSAS** — registros de atendimentos realizados pelos serviços de assistência social.

As bases foram posteriormente tratadas e transformadas utilizando o **Power Query**, diretamente no Power BI.

### 2. Tratamento dos dados

Durante a etapa de preparação dos dados, foram realizadas transformações necessárias para padronização e utilização das informações no modelo, incluindo:

* Tratamento e padronização de colunas;
* Ajustes de tipos de dados;
* Organização das informações cadastrais;
* Tratamento de informações territoriais;
* Preparação das tabelas para relacionamento;
* Criação de campos auxiliares para análise.

### 3. Modelagem dos dados

Foi utilizada uma **modelagem dimensional baseada no modelo estrela**, separando informações de dimensão e fatos.

Entre as principais tabelas de dimensão utilizadas estão:

* `dim_pessoa`
* `dim_territorio`
* `calendario`
* `dim_salario_minimo`

Os relacionamentos foram estruturados utilizando cardinalidades de **1:N (um para muitos)**, permitindo organizar as diferentes fontes de dados e manter a consistência do modelo.

Também foram desenvolvidas medidas em **DAX** para obtenção dos principais indicadores do relatório, incluindo:

* Quantidade de pessoas;
* Quantidade de atendimentos;
* Indicadores de renda;
* Classificação por faixa de renda;
* Indicadores temporais.

Para a análise de renda, foi criada a `dim_salario_minimo`, utilizada como referência para o cálculo das faixas de renda considerando a variação do salário mínimo ao longo dos anos.

## Visões do dashboard

### Renda

Esta visão apresenta uma análise geral da distribuição de renda da população atendida.

Entre os principais indicadores estão:

* Distribuição por sexo;
* Distribuição por raça;
* Distribuição por faixa de renda;
* Evolução dos atendimentos ao longo do tempo;
* Relação entre atendimentos e faixas de renda.

A página também permite realizar análises utilizando filtros como **ano, bairro e CRAS**.

### CRAS

Apresenta indicadores relacionados aos atendimentos realizados pelos **Centros de Referência de Assistência Social (CRAS)**.

A visão contempla:

* Pirâmide etária;
* Evolução dos atendimentos ao longo do tempo;
* Distribuição dos atendimentos por unidade;
* Distribuição por raça.

### CREAS

Apresenta indicadores relacionados aos atendimentos realizados pelos **Centros de Referência Especializados de Assistência Social (CREAS)**.

Entre as análises disponíveis estão:

* Pirâmide etária;
* Evolução dos atendimentos;
* Distribuição por unidade;
* Distribuição por raça.

### Conselho Tutelar

Apresenta indicadores relacionados aos atendimentos realizados pelo **Conselho Tutelar (CT)**.

A visão permite analisar:

* Pirâmide etária;
* Evolução dos atendimentos ao longo do tempo;
* Distribuição por unidade;
* Distribuição por raça.

### Centro POP

Apresenta indicadores relacionados aos atendimentos realizados pelo **Centro de Referência Especializado para População em Situação de Rua (Centro POP)**.

A página apresenta:

* Pirâmide etária;
* Evolução dos atendimentos;
* Distribuição por unidade;
* Distribuição por raça.

## Estrutura do projeto

```text
Indicadores-Hogwarts/
│
├── README.md
├── PowerBI/
│   └── Indicadores Hogwarts.pbix
│
├── Dados/
│   └── cecad_harry_potter_ficticio.csv
│   └── BPC_harry_potter_ficticio.csv
│   └── irsas_harry_potter_ficticio.csv
└── Imagens/
    └── ministerio da magia.png
```

## Observação sobre os dados

Este repositório **não contém dados reais ou informações pessoais**.

Todos os dados utilizados na versão pública foram criados artificialmente exclusivamente para demonstrar as funcionalidades e a estrutura analítica do dashboard.

A temática de *Harry Potter* foi utilizada apenas como recurso para diferenciação e demonstração do projeto.
