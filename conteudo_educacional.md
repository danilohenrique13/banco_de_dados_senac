# 📘 Conteúdo Educacional: SQL DDL e DML

Este documento visa explicar os dois grupos mais importantes de comandos SQL utilizados na gestão de bancos de dados: **DDL (Data Definition Language)** e **DML (Data Manipulation Language)**.

Usaremos exemplos práticos extraídos do projeto do Mercadinho para ilustrar como eles funcionam.

---

## 1. DDL: Data Definition Language (Linguagem de Definição de Dados)

A DDL é responsável por **definir, modificar ou remover a estrutura** do banco de dados e seus objetos (como tabelas, índices e esquemas). Ela atua no *esquema* (estrutura) e não nos dados internos.

| Comando | Propósito | Exemplo Prático (DDL do Mercadinho) |
| :--- | :--- | :--- |
| **CREATE** | Cria um novo objeto no banco de dados. | `CREATE TABLE PRODUTOS (...)` |
| **ALTER** | Modifica a estrutura de um objeto existente. | `ALTER TABLE PRODUTOS ADD COLUMN Peso DECIMAL(5,2);` (Adiciona uma nova coluna) |
| **DROP** | Remove um objeto inteiro do banco de dados (tabela, visão, etc.). | `DROP TABLE VENDAS;` (Remove a tabela permanentemente) |
| **TRUNCATE** | Remove **todos os dados** de uma tabela, mas mantém a sua estrutura. | `TRUNCATE TABLE CLIENTES;` (Limpa todos os registros de clientes) |

### 💡 Exemplo de Criação de Tabela (CREATE TABLE)

Este comando cria a tabela `CLIENTES` e define suas colunas e restrições:

```sql
CREATE TABLE CLIENTES (
    ClienteID INT PRIMARY KEY,         -- Define ClienteID como Chave Primária (PK)
    Nome VARCHAR(100) NOT NULL,        -- Define que o Nome não pode ser nulo
    Telefone VARCHAR(15),
    Email VARCHAR(100) UNIQUE          -- Define que o Email deve ser único no banco
);
```

### 2. DML: Data Manipulation Language (Linguagem de Manipulação de Dados)

A DML é responsável por **manipular os dados** contidos dentro das tabelas.  
Ela permite inserir, recuperar, atualizar e excluir registros (linhas).

## Tabela de Comandos DML

| Comando | Propósito | Exemplo Prático (DML do Mercadinho) |
|--------|-----------|--------------------------------------|
| **INSERT** | Adiciona novos registros (linhas) a uma tabela. | `INSERT INTO CLIENTES (...) VALUES (...)` |
| **SELECT** | Recupera dados de uma ou mais tabelas. | `SELECT Nome, PrecoVenda FROM PRODUTOS;` |
| **UPDATE** | Modifica valores de dados existentes em um ou mais registros. | `UPDATE PRODUTOS SET PrecoVenda = 16.28 WHERE Nome = 'Café Torrado 500g';` |
| **DELETE** | Remove registros (linhas) de uma tabela. | `DELETE FROM CLIENTES WHERE Nome = 'Bruno Lima';` |

---

## 2.1 Exemplo de Inserção de Dados (INSERT INTO)

Este comando DML insere um novo registro na tabela **FORNECEDORES**:

```sql
INSERT INTO FORNECEDORES (FornecedorID, Nome, Telefone, Endereco) 
VALUES (103, 'Padaria Central', '(81) 4444-5555', 'Rua Do Pão, 30');
```

## 2.2 Exemplo de Atualização de Dados (UPDATE)

Este comando DML modifica o preço de um produto existente.  
A cláusula **WHERE** é essencial para definir quais registros serão afetados:

```sql
UPDATE PRODUTOS 
SET PrecoVenda = PrecoVenda * 1.05  -- Aumenta o preço em 5%
WHERE Nome = 'Café Torrado 500g';   -- SOMENTE para o produto Café
```

## 2.3 Exemplo de Consulta de Dados (SELECT)

Este comando DML recupera o nome do cliente e o valor total de todas as vendas realizadas por ele:

```sql
SELECT C.Nome, V.ValorTotal, V.DataHora
FROM VENDAS V
JOIN CLIENTES C ON V.ClienteID = C.ClienteID
ORDER BY V.DataHora DESC;
```

