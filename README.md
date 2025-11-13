# Banco de Dados – Mercadinho

Este repositório contém a atividade acadêmica sobre **comandos DDL e DML** em SQL.  
O objetivo é criar um banco de dados para um mercadinho fictício, com modelagem, scripts SQL e material educativo.

---

## Objetivo do projeto

- Criar um banco de dados simples (mercadinho) usando comandos **DDL** e **DML**.
- Demonstrar modelagem, criação de tabelas, chaves e relacionamentos.
- Inserir dados de exemplo e explicar os comandos utilizados.
- Organizar o projeto em um repositório GitHub.

---

## Sobre o banco de dados

O banco de dados modela um mercadinho de bairro e inclui as seguintes tabelas:

- `Categorias` — tipos de produtos (ex.: Bebidas, Alimentos).
- `Produtos` — itens disponíveis para venda.
- `Clientes` — cadastro de clientes.
- `Vendas` — registro de cada venda realizada.
- `ItensVenda` — produtos que compõem cada venda.

Relacionamentos principais:

- `Categorias` 1 → N `Produtos`  
- `Clientes` 1 → N `Vendas`  
- `Vendas` 1 → N `ItensVenda`  
- `Produtos` 1 → N `ItensVenda`

---

## Arquivos do repositório

- `/sql_scripts/mercadinho.sql` — script completo (DDL + DML).  
- `conteudo_educacional.md` — explicação sobre DDL e DML.  
- `README.md` — este arquivo.

---

## Como executar

1. Abra seu gerenciador SQL (ex.: MySQL Workbench, HeidiSQL, DBeaver).  
2. Abra o arquivo `/sql_scripts/mercadinho.sql`.  
3. Execute todo o script. Ele criará o banco `mercadinho`, as tabelas e inserirá dados de exemplo.

---


## Autor / Contato

- Nome: Danilo Henrique Basilio da Silva  
- Email: danilo.silva5967574@edu.pe.senac.br

