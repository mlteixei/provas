# Comandos SQL

| Banco de Dados | Comando SQL para Criar Tabela                                     |
| -------------- | -------------------------------------------------- |
| MySQL          | ```sql CREATE TABLE empregado (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(255), departamento_id INT, FOREIGN KEY (departamento_id) REFERENCES departamento(id)); ``` |
| PostgreSQL     | ```sql CREATE TABLE empregado (id SERIAL PRIMARY KEY, nome VARCHAR(255), departamento_id INT REFERENCES departamento(id)); ``` |
| SQL Server     | ```sql CREATE TABLE empregado (id INT IDENTITY(1,1) PRIMARY KEY, nome NVARCHAR(255), departamento_id INT REFERENCES departamento(id)); ``` |
| Oracle         | ```sql CREATE TABLE empregado (id NUMBER GENERATED BY DEFAULT ON NULL AS IDENTITY PRIMARY KEY, nome VARCHAR2(255), departamento_id NUMBER REFERENCES departamento(id)); ``` |

| Banco de Dados | Comando SQL para Inserir Chave Primária                                      | Comando SQL para Remover Chave Primária                                  |
| -------------- | ----------------------------------------------- | ----------------------------------------------------------------------- |
| MySQL          | ```sql ALTER TABLE empregado ADD PRIMARY KEY (cpf); ``` | ```sql ALTER TABLE nome_tabela DROP PRIMARY KEY; ```                    |
| PostgreSQL     | ```sql ALTER TABLE empregado ADD PRIMARY KEY (cpf); ``` | ```sql ALTER TABLE nome_tabela DROP CONSTRAINT nome_chave_primaria; ``` |
| SQL Server     | ```sql ALTER TABLE empregado ADD CONSTRAINT PK_empregado_cpf PRIMARY KEY (cpf); ``` | ```sql ALTER TABLE nome_tabela DROP CONSTRAINT nome_chave_primaria; ``` |
| Oracle         | ```sql ALTER TABLE empregado ADD CONSTRAINT PK_empregado_cpf PRIMARY KEY (cpf); ``` | ```sql ALTER TABLE nome_tabela DROP PRIMARY KEY; ```                    |

| Banco de Dados | Comando SQL para Inserir Coluna | Comando SQL para Excluir Coluna                                                       | Comando SQL para Modificar Coluna                       |
| -------------- | --------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------ |
| MySQL          | ```sql ALTER TABLE empregado ADD COLUMN salario DECIMAL(10,2); ``` | ```sql ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ``` | ```sql ALTER TABLE nome_tabela MODIFY nome_coluna novo_tipo; ``` |
| PostgreSQL     | ```sql ALTER TABLE empregado ADD COLUMN salario DECIMAL(10,2); ``` | ```sql ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ``` | ```sql ALTER TABLE nome_tabela ALTER COLUMN nome_coluna TYPE novo_tipo; ``` |
| SQL Server     | ```sql ALTER TABLE empregado ADD salario DECIMAL(10,2); ```      | ```sql ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ``` | ```sql ALTER TABLE nome_tabela ALTER COLUMN nome_coluna novo_tipo; ``` |
| Oracle         | ```sql ALTER TABLE empregado ADD salario NUMBER(10,2); ```       | ```sql ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ``` | ```sql ALTER TABLE nome_tabela MODIFY nome_coluna novo_tipo; ``` |


| Banco de Dados | Comando SQL para Adicionar Restrição                             | Comando SQL para Remover Restrição                                      |
| -------------- | -------------------------------------------------------------- | ----------------------------------------------------------------------- |
| MySQL          | ```sql ALTER TABLE nome_tabela ADD CONSTRAINT nome_restrição CHECK (condição); ``` | ```sql ALTER TABLE nome_tabela DROP CONSTRAINT nome_restrição; ```      |
| PostgreSQL     | ```sql ALTER TABLE nome_tabela ADD CONSTRAINT nome_restrição CHECK (condição); ``` | ```sql ALTER TABLE nome_tabela DROP CONSTRAINT nome_restrição; ```      |
| SQL Server     | ```sql ALTER TABLE nome_tabela ADD CONSTRAINT nome_restrição CHECK (condição); ``` | ```sql ALTER TABLE nome_tabela DROP CONSTRAINT nome_restrição; ```      |
| Oracle         | ```sql ALTER TABLE nome_tabela ADD CONSTRAINT nome_restrição CHECK (condição); ``` | ```sql ALTER TABLE nome_tabela DROP CONSTRAINT nome_restrição; ```      |


| Banco de Dados | Comando SQL para Criar Usuário                  | Comando SQL para Conceder Permissões                  |
| -------------- | --------------------------------------------- | ----------------------------------------------------- |
| MySQL          | ```sql CREATE USER 'nome_usuario'@'localhost' IDENTIFIED BY 'senha'; ``` | ```sql GRANT permissao ON banco_de_dados.tabela TO 'nome_usuario'@'localhost'; ``` |
| PostgreSQL     | ```sql CREATE USER nome_usuario WITH PASSWORD 'senha'; ``` | ```sql GRANT permissao ON tabela TO nome_usuario; ``` |
| SQL Server     | ```sql CREATE LOGIN nome_usuario WITH PASSWORD = 'senha'; ``` | ```sql USE banco_de_dados; GRANT permissao ON tabela TO nome_usuario; ``` |
| Oracle         | ```sql CREATE USER nome_usuario IDENTIFIED BY senha; ``` | ```sql GRANT permissao ON tabela TO nome_usuario; ``` |

| Banco de Dados | Comando SQL para Criar Índices                                     |
| -------------- | ------------------------------------------------------------------ |
| MySQL          | ```sql CREATE INDEX nome_indice ON nome_tabela (nome_coluna); ```   |
| PostgreSQL     | ```sql CREATE INDEX nome_indice ON nome_tabela (nome_coluna); ```   |
| SQL Server     | ```sql CREATE INDEX nome_indice ON nome_tabela (nome_coluna); ```   |
| Oracle         | ```sql CREATE INDEX nome_indice ON nome_tabela (nome_coluna); ```   |
