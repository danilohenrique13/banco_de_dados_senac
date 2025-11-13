# 🏦 Banco de Dados - Mercadinho Da Dona Edinha

Este repositório contém um projeto prático de banco de dados SQL, focado na aplicação e entendimento dos comandos DDL (Data Definition Language) e DML (Data Manipulation Language).

O cenário escolhido para a modelagem foi um sistema básico para um **Mercadinho** fictício.

---

## 🎯 Objetivo do Projeto

O objetivo principal deste projeto foi consolidar a compreensão sobre:

1.  **Modelagem de Dados Simples:** Planejamento e definição de entidades (tabelas) e seus atributos, incluindo a identificação de chaves primárias e estrangeiras.
2.  **DDL na Prática:** Utilização dos comandos `CREATE TABLE` para construir a estrutura do banco de dados, definindo tipos de dados e restrições (`NOT NULL`, `PRIMARY KEY`, `FOREIGN KEY`).
3.  **DML na Prática:** Manipulação de dados utilizando `INSERT`, `SELECT`, `UPDATE` e `DELETE` para popular e gerenciar as informações do mercadinho.

## 💾 Estrutura do Banco de Dados: Mercadinho

O banco de dados do mercadinho é composto por quatro tabelas principais que gerenciam o estoque, fornecedores, clientes e histórico de transações:

| Tabela | Propósito | Chaves |
| :--- | :--- | :--- |
| **FORNECEDORES** | Dados de quem fornece os produtos. | `FornecedorID` (PK) |
| **CLIENTES** | Dados dos compradores. | `ClienteID` (PK) |
| **PRODUTOS** | Itens à venda. | `ProdutoID` (PK), `FornecedorID` (FK) |
| **VENDAS** | Histórico das transações. | `VendaID` (PK), `ClienteID` (FK) |

## 📁 Como Executar o Script SQL

O script completo para a criação e população do banco de dados está localizado na pasta `sql_scripts/`.

### Pré-requisitos
* Um SGBD (Sistema Gerenciador de Banco de Dados) instalado e configurado (ex: MySQL, PostgreSQL, SQLite).
* Um ambiente ou ferramenta para execução de comandos SQL (ex: DBeaver, MySQL Workbench, pgAdmin).

### Passos de Execução

1.  Acesse a pasta `sql_scripts/`.
2.  Abra o arquivo **`mercadinho_script.sql`**.
3.  Execute o script completo no seu ambiente SQL.

O script irá, em sequência:
1.  Criar as quatro tabelas definidas (DDL).
2.  Inserir dados de exemplo em todas as tabelas (DML).
3.  Demonstrar exemplos de comandos `UPDATE` e `SELECT` (DML).

## 📚 Conteúdo Educacional

Para uma explicação mais detalhada sobre os conceitos de DDL e DML e exemplos práticos dos comandos utilizados neste projeto, consulte o arquivo **`CONTEUDO_EDUCACIONAL.md`** neste repositório.

---

**Autor:** [Danilo H. B. da Silva]
**Status:** Concluído (Etapa 1: Criação de DB e Etapa 2: Configuração de Repositório)
