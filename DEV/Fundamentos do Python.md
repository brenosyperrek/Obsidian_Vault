# Primeiros Exemplos

```python
print('Hello Python!')

1\

    + 2
```


1 + 2 + 3

4 + 5 + 6

[2]:

15

[3]:

print(1 + 2 + 3)

print(4 + 5 + 6)

6
15

# Tipos Básicos[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Tipos-B%C3%A1sicos)

[4]:

print(True)

print(False)

print(1.2+1)

print('Aqui eu falo a minha lingua!')

print('Você é ' + 3 * 'muito ' + 'legal!')

# print (3 + '3') -> Ambiguidade

print([1,2,3])

print({'nome' : 'Pedro',"Idade" : 22})

print (None)

True
False
2.2
Aqui eu falo a minha lingua!
Você é muito muito muito legal!
[1, 2, 3]
{'nome': 'Pedro', 'Idade': 22}
None

# Variáveis[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Vari%C3%A1veis)

[5]:

a = 10

b = 5.2

​

print(a + b)

​

a = 'Agora sou uma string'

print(a)

15.2
Agora sou uma string

# Comentários[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Coment%C3%A1rios)

[6]:

# Minhas variáveis

​

salario = 3450.55

despesas = 1345.66

​

"""

    A idéia é calcular o quanto vai sobrar so salário

"""

​

print(salario - despesas)

2104.8900000000003

# Operadores Aritméticos[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Operadores-Aritm%C3%A9ticos)

[4]:

print(2 + 3)

print(4 - 7)

print(2 * 5.3)

print(9.4 / 3)

print(9.4 // 3)

print(2 ** 8)

print(10 % 3)

​

a = 12

b = a

print (a + b)

5
-3
10.6
3.1333333333333333
3.0
256
1
24

[7]:

# Minhas variáveis

salario = 3450.55

despesas = 1345.66

​

# Resposta do desafio

percentual = despesas / salario * 100

print(percentual)

38.99842054165278

# Operadores Relacionais[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Operadores-Relacionais)

[1]:

3 > 4

4 >= 3

1 < 2

3 <= 1

3 != 2

3 == 3

2 == '2'

[1]:

False

# Operadores de Atribuição[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Operadores-de-Atribui%C3%A7%C3%A3o)

[7]:

a = 3

a = a + 7

print(a)

​

a += 5 # a = a + 5

print(a)

​

a -= 3

print(a)

​

a *=2

print(a)

​

a /= 4

print(a)

​

a %= 4

print(a)

​

a **= 8

print(a)

​

a //= 255

print(a)

10
15
12
24
6.0
2.0
256.0
1.0

# Operadores Lógicos[](http://localhost:8888/lab/tree/Notas/fundamentos.ipynb#Operadores-L%C3%B3gicos)

[15]:

True or False

7 != 3 and 2 > 3

​

# Tabela verdade do operador AND

print(True and True)

print(True and False)

print(False and True)

print(False and False)

​

# Tabela verdade do operador OR

print(True or True)

print(True or False)

print(False or True)

print(False or False)

​

True
False
False
False
True
True
True
False