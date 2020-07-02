# <font color='blue'>Python Fundamentos - Capítulo 5</font>



```python
# Versão da Linguagem Python
from platform import python_version
print('Versão da Linguagem Python Usada Neste Jupyter Notebook:', python_version())
```

## Objetos

Em Python, tudo é objeto!


```python
# Criando uma lista
lst_num = ["Data", "Science", "Academy", "Nota", 10, 10]
```


```python
# A lista lst_num é um objeto, uma instância da classe lista em Python
type(lst_num)
```


```python
lst_num.count(10)
```


```python
# Usamos a função type, para verificar o tipo de um objeto
print(type(10))
print(type([]))
print(type(()))
print(type({}))
print(type('a'))
```

    <class 'int'>
    <class 'list'>
    <class 'tuple'>
    <class 'dict'>
    <class 'str'>
    


```python
# Criando um novo tipo de objeto chamado Carro
class Carro(object):
    pass

# Instância do Carro
palio = Carro()

print(type(palio))
```

    <class '__main__.Carro'>
    


```python
# Criando uma classe
class Estudantes:
    def __init__(self, nome, idade, nota):
        self.nome = nome
        self.idade = idade
        self.nota = nota
```


```python
# Criando um objeto chamado Estudante1 a partir da classe Estudantes
Estudante1 = Estudantes("Pele", 12, 9.5)
```


```python
# Atributo da classe Estudante, utilizado por cada objeto criado a partir desta classe
Estudante1.nome
```




    'Pele'




```python
# Atributo da classe Estudante, utilizado por cada objeto criado a partir desta classe
Estudante1.idade
```




    12




```python
# Atributo da classe Estudante, utilizado por cada objeto criado a partir desta classe
Estudante1.nota
```




    9.5




```python
# Criando uma classe
class Funcionarios:
    def __init__(self, nome, salario):
        self.nome = nome
        self.salario = salario

    def listFunc(self):
        print("O nome do funcionário é " + self.nome + " e o salário é R$" + str(self.salario))
```


```python
# Criando um objeto chamado Func1 a partir da classe Funcionarios
Func1 = Funcionarios("Obama", 20000)
```


```python
# Usando o método da classe
Func1.listFunc()
```

    O nome do funcionário é Obama e o salário é R$20000
    


```python
print("**** Usando atributos *****")
```

    **** Usando atributos *****
    


```python
hasattr(Func1, "nome")
```




    True




```python
hasattr(Func1, "salario")
```




    True




```python
setattr(Func1, "salario", 4500)
```


```python
hasattr(Func1, "salario")
```




    True




```python
getattr(Func1, "salario")
```




    4500




```python
delattr(Func1, "salario")
```


```python
hasattr(Func1, "salario")
```




    False


