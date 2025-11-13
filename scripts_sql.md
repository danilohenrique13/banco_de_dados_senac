-- #######################################################
-- # Etapa 1: Criação do Banco de Dados (DDL) #
-- #######################################################

-- 1. Tabela FORNECEDORES
CREATE TABLE FORNECEDORES (
    FornecedorID INT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Telefone VARCHAR(15),
    Endereco VARCHAR(255)
);

-- 2. Tabela CLIENTES
CREATE TABLE CLIENTES (
    ClienteID INT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Telefone VARCHAR(15),
    Email VARCHAR(100) UNIQUE 
);

-- 3. Tabela PRODUTOS
CREATE TABLE PRODUTOS (
    ProdutoID INT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    PrecoVenda DECIMAL(10, 2) NOT NULL,
    Estoque INT NOT NULL DEFAULT 0, 
    FornecedorID INT,
    
    FOREIGN KEY (FornecedorID) REFERENCES FORNECEDORES(FornecedorID)
);

-- 4. Tabela VENDAS
CREATE TABLE VENDAS (
    VendaID INT PRIMARY KEY,
    DataHora DATETIME NOT NULL,
    ValorTotal DECIMAL(10, 2) NOT NULL,
    ClienteID INT,
    
    FOREIGN KEY (ClienteID) REFERENCES CLIENTES(ClienteID)
);

-- #################################################################
-- # Etapa 1: Inserção de Dados (DML) #
-- #################################################################

-- FORNECEDORES
INSERT INTO FORNECEDORES (FornecedorID, Nome, Telefone, Endereco) VALUES
(101, 'Distribuidora ABC', '(11) 9876-5432', 'Rua Alfa, 100'),
(102, 'Laticínios Minas', '(21) 1234-5678', 'Av. Beta, 200');

-- CLIENTES
INSERT INTO CLIENTES (ClienteID, Nome, Telefone, Email) VALUES
(1, 'Ana Costa', '(11) 9999-0000', 'ana.costa@email.com'),
(2, 'Bruno Lima', '(11) 8888-1111', NULL);

-- PRODUTOS
INSERT INTO PRODUTOS (ProdutoID, Nome, PrecoVenda, Estoque, FornecedorID) VALUES
(1, 'Café Torrado 500g', 15.50, 50, 101),
(2, 'Leite Integral 1L', 5.99, 100, 102),
(3, 'Pão de Forma', 8.90, 30, 101);

-- VENDAS
INSERT INTO VENDAS (VendaID, DataHora, ValorTotal, ClienteID) VALUES
(5001, '2025-11-13 14:30:00', 21.49, 1), 
(5002, '2025-11-13 15:45:00', 8.90, 2), 
(5003, '2025-11-13 16:00:00', 50.00, 1);

-- ###################################################
-- # Etapa 1: Exemplos de Manipulação (DML) #
-- ###################################################

-- DML: UPDATE (Aumentar o preço do Café em 5%)
UPDATE PRODUTOS 
SET PrecoVenda = PrecoVenda * 1.05 
WHERE Nome = 'Café Torrado 500g';

-- DML: SELECT (Consultar vendas de um cliente)
SELECT V.*
FROM VENDAS V
JOIN CLIENTES C ON V.ClienteID = C.ClienteID
WHERE C.Nome = 'Ana Costa';
