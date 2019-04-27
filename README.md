# Anotações

## Diferença entre listas, tuplas, conjunto (set) e dicionários

### Listas

Lista é uma estrutura de dados em Python que pode ser assemelhada a __arrays__ de outras linguagens de programação, ela pode ser uma coleção de elementos de qualquer classe (`int`, `str`, `bool`, `list`, entre outros). Listas são indexáveis e ordenável.

Listas são criadas utilizando colchetes
```python
nome = ['Ricardo', 'Aparecido', 'Bezerra']
```
E acessada por índices
```python
nome[0]     # printa Ricardo
nome[2]     # printa Bezerra
```
As listas possuem [vários métodos](https://docs.python.org/2/tutorial/datastructures.html#more-on-lists). Os mais comuns é o `append` que adiciona um elemento ao final da lista.

```python
nome.append('Só')
print(nome)
['Ricardo', 'Aparecido', 'Bezerra', 'Só']
```

O método `extend` também adiciona elementos na lista, mas com uma "sutil" diferença

```python
nome.append(['Teste', 'Teeste'])
nome.extend(['Teste', 'Teeste'])
print(nome)
['Ricardo', 'Aparecido', 'Bezerra', 'Só', ['Teste', 'Teeste'], 'Teste', 'Teeste']
```
Note que o `append` adiciona de fato um elemento ao final da lista e `extend` estende a lista com os elementos novos.

**Importante**

Listas são clonadas, ou seja, possuem uma referência na memória

```python
lista1 = [1, 2, 'Oliveira', 4, True]
lista2 = lista1
```
Os objetos `lista1` e `lista2` estão apontando para o mesmo endereço e qualquer modificação feita em uma afetará a outra.
Para copiar o conteúdo de uma lista à outra podemos usar o fatiamento (__slicing__)

```python
lista3 = lista2[:]
print(lista2 is lista1)   # Retornará True
print(lista3 is lista2)   # Retornará False
```
Listas também pode ser utilizadas como pilhas, inclusive possui métodos específicos para isso.

Referências:
* Aulas USP de Ciência da Computação com Python [aqui](https://panda.ime.usp.br/aulasPython/static/aulasPython/aula09.html) e [aqui](https://panda.ime.usp.br/aulasPython/static/aulasPython/aula10.html)
* [Documentação do Python](https://docs.python.org/2/tutorial/datastructures.html#more-on-lists)
* [W3School List](https://www.w3schools.com/python/python_lists.asp)
