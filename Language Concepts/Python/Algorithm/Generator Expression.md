Uma expressão geradora é uma construção semelhante a [List Comprehension](./List%20Comprehension.md). Juntamente com ela, também existe a função geradora, que diferente da função comum ela possui uma instrução **yield** e retorna um objeto gerador.

- **yield** é uma instrução que torna uma função comum em uma função geradora. Quando chamamos uma função desse tipo, em vez dela retornar um objeto normalmente, ela retorna um objeto gerador que pode ser iterado e aí sim iremos ver os valores produzidos por ela.

Em grandes quantidades de dados, as funções geradoras são uteis pois geram valores sob comanda, tornando-as mais eficientes.

![](../../../Images/Python/Generator%20Expression/Pasted%20image%2020231221205521.png)

A sintaxe é bem parecida com [List Comprehension](List%20Comprehension.md), porém em vez de ser colchetes **[]**, se usa parênteses **()**:

```python
generatorExpression = (expressao for elemento in iteravel if condicao)
```

os significados dessa sintaxe ai eh a mema coisa da list comprehension, então nao vou colocar aqui de novo nao

Podemos usar tanto uma [função geradora](#^da6956) ou declarar uma expressão geradora.

# Expressão Geradora

```python
lstItarable = [2, 4, 6, 8, 10]

# criando uma expressao geradora que eleva todos os numeros da lista "lstItarable" ao quadrado
generatorExpression = (n ** 2 for i in lstItarable)

for i in generatorExpression: # iterando sobre o objeto
	print(i)
	# output:
	# 4
	# 16
	# 36
	# 64
	# 100
#
```


# Função geradora

^da6956

Vamos definir uma função que retorna um objeto gerador:
```python
# funcao que retorna todos os numeros ao quadrado

def quadractic(number: int) -> int: 
	for i in range(number):
		yield i ** 2 
		
		# yield tornando a funcao geradora, se usassemos o "return" ela seria uma funcao comum e nao precisariamos iterar sobre ela
```

Como ela retorna um objeto gerador, podemos iterar sobre o resultado com um for:

```python
for i in quadractic(6): # iterando do 0 ate o 5
	print(i, end=" ")
	# output: 0 1 4 9 16 25
	# retornou todos os numeros (do 0 ate o 5) elevados ao quadrado
	
```


# Links

https://www.pythontutorial.net/advanced-python/python-generator-expressions/

