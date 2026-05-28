<h1 align="center">🧾 Mini ERP Comercial Oracle</h1>
<p align="center">
Camada de banco de dados para simulação de ERP corporativo utilizando Oracle Database
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Oracle-Database-red?style=for-the-badge&logo=oracle&logoColor=white" alt="Oracle" />
  <img src="https://img.shields.io/badge/DBeaver-Universal%20Tool-379f46?style=for-the-badge&logo=dbeaver&logoColor=white" alt="DBeaver" />
  <img src="https://img.shields.io/badge/GitHub-Repositório-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  <img src="https://img.shields.io/badge/status-EM%20CONSTRUÇÃO-yellow?style=for-the-badge" alt="Status" />
</p>

## 📌 Visão Geral

**Mini ERP Comercial Oracle** é um projeto de estudo e portfólio que simula a camada de banco de dados de um sistema ERP (Enterprise Resource Planning) focado no módulo comercial.  

O projeto foi construído com **Oracle Database XE** e **DBeaver**, aplicando conceitos de:
- Modelagem relacional (DER, PK, FK, constraints)
- SQL para consultas e manipulação de dados
- PL/SQL para regras de negócio, procedures, funções e triggers
- Boas práticas de organização de scripts e versionamento (Git/GitHub)

A inspiração vem de sistemas ERP corporativos reais, como os da **TOTVS**, com o objetivo de demonstrar habilidade prática para vagas júnior/trainee no ecossistema ERP.

---

## 🎯 Público-Alvo e Objetivos de Carreira

Este projeto é direcionado a:

- **Desenvolvedores e analistas de sistemas** que desejam ver um exemplo estruturado de implementação de banco de dados corporativo.
- **Avaliadores de portfólio** que buscam evidências de modelagem, lógica de negócio e organização.

**Meu objetivo** com este projeto:
- Consolidar conhecimentos de SQL Oracle em um caso realista.
- Mostrar capacidade de modelar um domínio de negócio (vendas, estoque, faturamento).
- Criar material público que sirva como diferencial competitivo em processos seletivos.

---

## 🧰 Stack Tecnológica

| Camada          | Tecnologia                               |
|----------------|------------------------------------------|
| Banco de Dados | Oracle Database XE 18c/21c               |
| IDE/Cliente    | DBeaver (Universal Database Tool)        |
| Linguagem      | SQL, PL/SQL                              |
| Versionamento  | Git + GitHub                             |
| Documentação   | Markdown, draw.io (DER)                  |



## 🚀 Funcionalidades
- Cadastro de clientes
- Cadastro de produtos
- Controle de pedidos
- Movimentação de estoque
- Relatórios comerciais
- Procedures PL/SQL
- Triggers para automações
- Views analíticas

## 📐 Modelagem do Banco de Dados

### Entidades principais

1. **CLIENTES** – Cadastro de clientes (Pessoa Física ou Jurídica)
2. **VENDEDORES** – Equipe comercial, comissões e metas
3. **PRODUTOS** – Catálogo de produtos, preço, estoque
4. **PEDIDOS** – Cabeçalho das vendas
5. **ITENS_PEDIDO** – Itens de cada pedido
6. **ESTOQUE_MOVIMENTACAO** – Histórico de entradas e saídas

### Relacionamentos

- Um **CLIENTE** pode ter muitos **PEDIDOS** (1:N)
- Um **VENDEDOR** pode ter muitos **PEDIDOS** (1:N)
- Um **PEDIDO** pode ter muitos **ITENS_PEDIDO** (1:N)
- Um **PRODUTO** pode aparecer em muitos **ITENS_PEDIDO** e em muitas **ESTOQUE_MOVIMENTACAO**

> 🔜 O diagrama completo (Entidade-Relacionamento) está em `docs/diagrama_der.png` e foi criado com draw.io.

---

## 🗂️ Estrutura do Repositório

## Estrutura do repositório
```text
mini-erp-oracle/
│
├── README.md
├── .gitignore
│
├── docs/
│   ├── diagrams/
│   │   ├── er_diagram.drawio
│   │   └── er_diagram.png
│   │
│   ├── screenshots/
│   │   ├── dbeaver_tables.png
│   │   ├── consultas_sql.png
│   │   └── relatorios.png
│   │
│   └── roadmap/
│       └── roadmap.md
│
├── sql/
│   ├── 01_ddl/
│   │   ├── 01_clientes.sql
│   │   ├── 02_vendedores.sql
│   │   ├── 03_produtos.sql
│   │   ├── 04_pedidos.sql
│   │   ├── 05_itens_pedido.sql
│   │   ├── 06_estoque_movimentacao.sql
│   │   └── 07_constraints.sql
│   │
│   ├── 02_dml/
│   │   ├── insert_clientes.sql
│   │   ├── insert_vendedores.sql
│   │   ├── insert_produtos.sql
│   │   ├── insert_pedidos.sql
│   │   └── insert_itens_pedido.sql
│   │
│   ├── 03_queries/
│   │   ├── clientes_ativos.sql
│   │   ├── produtos_sem_estoque.sql
│   │   ├── relatorio_vendas.sql
│   │   ├── ranking_vendedores.sql
│   │   ├── faturamento_mensal.sql
│   │   └── ticket_medio.sql
│   │
│   ├── 04_views/
│   │   ├── vw_relatorio_vendas.sql
│   │   ├── vw_ranking_vendedores.sql
│   │   └── vw_faturamento_mensal.sql
│   │
│   ├── 05_procedures/
│   │   ├── sp_realizar_pedido.sql
│   │   └── sp_atualizar_estoque.sql
│   │
│   ├── 06_functions/
│   │   ├── fn_total_cliente.sql
│   │   └── fn_total_vendedor.sql
│   │
│   └── 07_triggers/
│       ├── trg_atualiza_estoque.sql
│       └── trg_auditoria_pedido.sql
│
└── assets/
    └── banner_projeto.png
