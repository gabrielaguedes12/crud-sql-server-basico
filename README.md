# crud-sql-server-basico
Revisão e prática de comandos SQL Server com foco em CRUD (Create, Read, Update, Delete) e organização de dados para backend.

# 🧠 Prática de CRUD com SQL Server

Este projeto tem como objetivo consolidar os fundamentos de SQL Server por meio da prática do CRUD completo: **Create**, **Read**, **Update** e **Delete**, simulando um sistema simples de gerenciamento de clientes e contas bancárias.

---

## 🛠️ Tecnologias Utilizadas

- SQL Server Management Studio (SSMS)
- Banco de dados relacional
- Comandos SQL puros

---

## 🧩 Estrutura das Tabelas

### 📄 Tabela Clientes
```sql
CREATE TABLE Clientes (
  id_cliente INT IDENTITY(1,1) PRIMARY KEY,
  nome VARCHAR(100) NOT NULL,
  email VARCHAR(100),
  cpf VARCHAR(20),
  data_criacao DATETIME DEFAULT GETDATE()
);

/*CREATE-insert*/
INSERT INTO Clientes(nome,email, cpf)
VALUES ('Eduardo Santos','edusant@gmail.com', '12345678934');

INSERT INTO Contas(id_cliente, numero_conta, tipo_conta)
VALUES (2,'147852-6','corrente');

INSERT INTO transacao (id_conta, tipo_transacao, valor)
VALUES (7, 'entrada', 500.00);

/*READ-select*/
SELECT * FROM Clientes;
SELECT * FROM Contas;
SELECT * FROM Transacao;

/*UPDATE*/
UPDATE Clientes
SET nome='Maria Silva'
WHERE id_cliente=2;

UPDATE contas
SET ativa = 0
WHERE id_conta = 4;

UPDATE Transacao
SET tipo_transacao = 'saida'
Where id_transacao=1;

/*DELETE-deletar*/
delete from Contas
WHERE id_conta = 4;

/*JOIN*/
SELECT c.nome, co.numero_conta, co.saldo
FROM contas co
JOIN clientes c ON co.id_cliente = c.id_cliente;

SELECT 
  co.numero_conta, 
  t.tipo_transacao, 
  t.valor, 
  t.data_transacao
FROM 
  Transacao t
JOIN 
  Contas co ON t.id_conta = co.id_conta;

  SELECT 
  c.nome, 
  co.numero_conta, 
  t.tipo_transacao, 
  t.valor, 
  t.data_transacao
FROM 
  Clientes c
JOIN 
  Contas co ON c.id_cliente = co.id_cliente
JOIN 
  Transacao t ON co.id_conta = t.id_conta;

```
### Prints das Operações
![Captura de tela 2025-06-26 232840](https://github.com/user-attachments/assets/5471e76f-db2c-49b0-8f31-675ffa7a9af7)

![Captura de tela 2025-06-26 233154](https://github.com/user-attachments/assets/68698c34-c9f5-4937-aa2a-c4f530733b80)

![Captura de tela 2025-06-26 232915](https://github.com/user-attachments/assets/31e9785f-bb22-49ce-9309-5ed5e28cd673)

🎯 Objetivo
Esse projeto é parte de um plano de estudos com foco em backend. A prática com comandos SQL visa consolidar fundamentos para integrar futuramente com APIs desenvolvidas em Java + Spring Boot.

## 👩‍💻 Autora

Gabriela Guedes — https://github.com/gabrielaguedes12
Projeto feito como parte do plano de estudos de backend com Java e Spring Boot.
