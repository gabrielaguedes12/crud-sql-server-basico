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

![Captura de tela 2025-06-26 232840](https://github.com/user-attachments/assets/5471e76f-db2c-49b0-8f31-675ffa7a9af7)

![Captura de tela 2025-06-26 233154](https://github.com/user-attachments/assets/68698c34-c9f5-4937-aa2a-c4f530733b80)

![Captura de tela 2025-06-26 232915](https://github.com/user-attachments/assets/31e9785f-bb22-49ce-9309-5ed5e28cd673)
