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
