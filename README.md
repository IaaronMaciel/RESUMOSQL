# RESUMOSQL
O que é NVARCHAR?
NVARCHAR é um tipo de dado no SQL Server usado para armazenar textos.
O "N" significa "National" — ou seja, ele suporta qualquer idioma, inclusive acentos, caracteres especiais (tipo "ç", "é", "ñ", "ü"), emojis, etc.
Tipo | Suporta acentuação? | Usa mais espaço? | Quando usar?
VARCHAR | NÃO | Menos espaço | Só textos sem acento (inglês)
NVARCHAR | SIM | Um pouco mais | Textos com acento ou multilíngue

O que é uma string?
String é simplesmente um conjunto de caracteres.
Ou seja: qualquer sequência de letras, números, símbolos ou espaços.

Exemplos de strings:
"Olá mundo"
"12345"
"R$ 50,00"
"Ana Maria"
"senha@123"

➡️ Tudo isso são strings porque são textos, mesmo que contenham números ou símbolos.
🔥 Imagina assim:
Uma string é como uma frase ou palavra guardada no computador.
O computador entende string como texto puro, e não como número para cálculo, por exemplo.
No SQL Server, usamos tipos como VARCHAR, NVARCHAR, CHAR, para armazenar strings.
Em linguagens de programação (Python, C#, Java etc.), a string também é uma variável de texto.
Exemplo em SQL:
INSERT INTO Usuarios (Nome) VALUES (N'João da Silva');
Aqui 'João da Silva' é uma string.

Exemplo em Python:

python
nome = "João da Silva"
print(nome)
Aqui "João da Silva" também é uma string.
 | 
🎯 Resumo curto:
String = texto ou sequência de caracteres. | 
Pode ter letras, números, espaços e símbolos. | 
Não é número para cálculo! | 


---------------------------------------------------------------------------------------------------
📚 O que é o comando INSERT INTO?
O INSERT INTO é um comando SQL usado para inserir novos dados dentro de uma tabela do banco de dados.

Em português:
→ INSERT INTO significa "inserir dentro de".

🛠️ Estrutura do comando
INSERT INTO NomeDaTabela (Coluna1, Coluna2, Coluna3)
VALUES (Valor1, Valor2, Valor3);
NomeDaTabela = nome da tabela onde você quer inserir os dados.

Coluna1, Coluna2, Coluna3 = as colunas que vão receber os valores.

Valor1, Valor2, Valor3 = os dados que você quer gravar.

🎯 Exemplo prático
Suponha que você tem essa tabela:

sql
Copiar
Editar
CREATE TABLE Pessoas (
    Id INT IDENTITY(1,1) PRIMARY KEY,
    Nome NVARCHAR(100),
    Cidade NVARCHAR(100),
    RG NVARCHAR(20)
);
Para adicionar uma nova pessoa na tabela, você usa:

sql
Copiar
Editar
INSERT INTO Pessoas (Nome, Cidade, RG)
VALUES ('Maria Oliveira', 'Fortaleza', '12.345.678-9');
O que acontece:

Nome vai receber "Maria Oliveira".

Cidade vai receber "Fortaleza".

RG vai receber "12.345.678-9".

🧠 Dica rápida:
Sempre escreva INSERT INTO para inserir novos registros.

O número de colunas deve bater com o número de valores.

Se a tabela tem um Id automático (como IDENTITY(1,1)), não precisa colocar o valor do Id, o SQL Server gera sozinho.

🚀 Resumo rápido:

INSERT INTO = inserir novos dados em uma tabela.	
Você informa quais colunas e quais valores.	
Muito usado para cadastrar novos registros.


------------------------------------------------------------------------------------------------------------------

Quando você quer adicionar uma nova coluna em uma tabela já existente.
Comando certo para adicionar uma nova coluna:
sql
Copiar
Editar
ALTER TABLE Pessoas
ADD Bairro NVARCHAR(100);
📚 Explicação:
ALTER TABLE = alterar uma tabela que já existe.

ADD = adicionar uma nova coluna.

Bairro NVARCHAR(100) = define o nome da coluna e o tipo de dado (texto de até 100 caracteres).

🎯 Exemplo completo:
sql
Copiar
Editar
-- Adicionar a coluna Bairro na tabela Pessoas
ALTER TABLE Pessoas
ADD Bairro NVARCHAR(100);
Depois disso, você pode fazer:

sql
Copiar
Editar
UPDATE Pessoas
SET Bairro = 'Centro'
WHERE Id = 1;
(ou inserir bairros novos quando adicionar registros.)

🚨 Cuidado:
Se tentar usar CREATE TABLE Pessoas de novo, vai sempre dar erro ("Tabela já existe"), porque o SQL Server não deixa recriar uma tabela que já existe.
