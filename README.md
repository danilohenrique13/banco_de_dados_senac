# 🛒 bank_de_dados_senac - Mercadinho do Bairro

## 📝 Descrição do Projeto

Este projeto consiste na criação de um banco de dados relacional simples para simular a gestão de um **Mercadinho de Bairro**. O foco é aplicar os conceitos de DDL (Linguagem de Definição de Dados) e DML (Linguagem de Manipulação de Dados) do SQL.

O banco de dados foi modelado para gerenciar as entidades centrais do negócio, incluindo o controle de estoque, o registro de vendas e, crucialmente, o controle de **dívidas ("fiado")** dos clientes.

## 🎯 Objetivo de Aprendizagem

Ao concluir este projeto, foram alcançados os seguintes objetivos:

1.  **Modelagem de Dados:** Planejar e estruturar entidades e relacionamentos para um cenário de negócio real (Mercadinho).
2.  **DDL (Data Definition Language):** Utilizar comandos `CREATE TABLE` para definir a estrutura do banco de dados, incluindo chaves primárias (`PRIMARY KEY`) e chaves estrangeiras (`FOREIGN KEY`).
3.  **DML (Data Manipulation Language):** Utilizar o comando `INSERT INTO` para popular as tabelas com dados de exemplo, simulando as operações diárias do mercadinho.
4.  **Organização de Projeto:** Criar e configurar um repositório GitHub para hospedar o projeto e o conteúdo educacional.

## 📂 Estrutura do Banco de Dados (Esquema)

O banco de dados é composto pelas seguintes tabelas:

| Tabela | Função | Principais Colunas |
| :--- | :--- | :--- |
| **Clientes** | Registro de informações cadastrais dos clientes. | `ClienteID` (PK), `Nome`, `Telefone` |
| **Produtos** | Catálogo de itens vendidos, preços e estoque. | `ProdutoID` (PK), `Nome`, `PrecoVenda`, `Estoque` |
| **Vendas** | Histórico das transações, incluindo o tipo de pagamento. | `VendaID` (PK), `DataHora`, `ClienteID` (FK), `TipoPagamento` |
| **Dividas** | Controle detalhado das transações realizadas como "fiado". | `DividaID` (PK), `ClienteID` (FK), `ValorDevido`, `Status` |

## 🚀 Como Executar o Script SQL

Para recriar este banco de dados em seu ambiente:

1.  **Pré-requisito:** Tenha um sistema de gerenciamento de banco de dados SQL instalado (ex: MySQL, PostgreSQL, SQL Server, SQLite).
2.  **Acesse o Script:** O arquivo SQL contendo todos os comandos de criação e inserção de dados está localizado na pasta `sql_scripts/`.
3.  **Execução:**
    * Abra o seu cliente SQL (terminal ou interface gráfica).
    * Crie um novo banco de dados (se necessário, dependendo do SGBD).
    * Execute sequencialmente os comandos contidos no arquivo `mercadinho_setup.sql` (ou o nome que você deu ao seu script).

> **Observação:** O script é escrito em SQL padrão, mas pode requerer pequenos ajustes sintáticos dependendo do SGBD específico utilizado.

---

## 📚 Conteúdo Educacional

*(Esta seção será preenchida com o conteúdo educacional que explica DDL e DML, conforme solicitado no **Estágio 2, Passo 3**.)*
