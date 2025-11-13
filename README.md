# Banco de Dados – Mercadinho

Este projeto faz parte da atividade acadêmica de exploração dos comandos **DDL** e **DML** em SQL, a Atividade foi proposta pela Professora Tereza Cristina na UC: Banco de Dados durante o 1º Período do Curso de Análise e Desenvolvimento de Sistemas da Faculdade SENAC.
O objetivo é criar um banco de dados para um negócio fictício, desenvolver o script SQL completo e organizar o projeto em um repositório GitHub.

---

## 📌 Objetivo do Projeto
- Criar um banco de dados simples utilizando DDL e DML.
- Aplicar conhecimentos de modelagem, criação de tabelas, chaves e relacionamentos.
- Demonstrar a criação e manipulação de dados usando SQL.
- Publicar o trabalho em um repositório GitHub bem organizado.

---

## 🏪 Sobre o Banco de Dados – Mercadinho

O banco de dados representa um mercadinho de bairro, escolhi este negócio pois minha família possui um mercadinho e acho que posso ajudá-los dessa forma. 
Ele é composto por cinco tabelas principais:

- **Categorias** – tipos de produtos (alimentos, bebidas etc.)
- **Produtos** – itens disponíveis para venda
- **Clientes** – pessoas cadastradas no sistema
- **Vendas** – registro de cada compra realizada
- **ItensVenda** – produtos que fazem parte de cada venda

Todos os relacionamentos foram planejados para manter a integridade das informações.

---

## 📊 Modelagem do Banco de Dados

### Tabelas criadas:
- Categorias (1 → N) Produtos  
- Clientes (1 → N) Vendas  
- Vendas (1 → N) ItensVenda  
- Produtos (1 → N) ItensVenda  

O esquema contém chaves primárias, estrangeiras e colunas essenciais para o gerenciamento básico do mercadinho.

---

## 📁 Onde está o Script SQL?

O script completo encontra-se na pasta:


