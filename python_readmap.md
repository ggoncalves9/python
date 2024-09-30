
# Python Study Guide

## Básico

### Introdução ao Python
Python é uma linguagem de programação de alto nível, interpretada e de fácil leitura. Seu design prioriza a simplicidade e a legibilidade, tornando-o uma excelente escolha para iniciantes e profissionais. Exemplo básico:

```python
# Hello World em Python
print("Hello, World!")
```

### Variáveis e Tipos de Dados
As variáveis em Python são criadas quando você atribui um valor a elas. Python é uma linguagem de tipagem dinâmica.

```python
x = 10        # Inteiro
y = 3.14      # Float
name = "Ana"  # String
is_valid = True  # Boolean
```

### Operadores
Python suporta operadores aritméticos, relacionais e lógicos.

```python
a = 10
b = 5

# Operadores aritméticos
soma = a + b
subtracao = a - b

# Operadores relacionais
maior = a > b  # True

# Operadores lógicos
condicao = (a > 0 and b > 0)  # True
```

### Estruturas Condicionais
As estruturas condicionais controlam o fluxo do programa com base em condições.

```python
idade = 18
if idade >= 18:
    print("Você é maior de idade.")
else:
    print("Você é menor de idade.")
```

### Loops
Loops permitem a execução repetida de um bloco de código. Python suporta `for` e `while`.

```python
# Loop for
for i in range(5):
    print(i)

# Loop while
count = 0
while count < 5:
    print(count)
    count += 1
```

### Funções
Funções permitem reutilizar blocos de código. Em Python, funções são definidas usando `def`.

```python
def saudacao(nome):
    return f"Olá, {nome}!"

print(saudacao("Ana"))
```

### Listas
Listas são coleções mutáveis de itens.

```python
numeros = [1, 2, 3, 4, 5]
print(numeros[0])  # Acessa o primeiro elemento
```

### Tuplas
Tuplas são coleções imutáveis.

```python
cores = ("vermelho", "verde", "azul")
print(cores[1])  # Acessa o segundo elemento
```

### Dicionários
Dicionários armazenam pares chave-valor.

```python
aluno = {"nome": "Ana", "idade": 22}
print(aluno["nome"])  # Acessa o valor associado à chave "nome"
```

### Conjuntos
Conjuntos são coleções não ordenadas de itens únicos.

```python
frutas = {"maçã", "banana", "laranja"}
```

### Manipulação de Strings
Python oferece várias formas de manipular strings.

```python
mensagem = "Olá, Mundo!"
print(mensagem.upper())  # Converte para maiúsculas
```

### Manipulação de Arquivos
É possível abrir e manipular arquivos com Python.

```python
with open("arquivo.txt", "r") as file:
    conteudo = file.read()
```

### Tratamento de Exceções
Exceções permitem tratar erros de forma controlada.

```python
try:
    x = int(input("Digite um número: "))
except ValueError:
    print("Entrada inválida. Digite um número.")
```

### Módulos e Pacotes
Python permite organizar o código em módulos e pacotes.

```python
# Importando um módulo
import math
print(math.sqrt(16))
```

## Avançado

### Programação Orientada a Objetos
Python suporta a Programação Orientada a Objetos (POO). Exemplo básico:

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def apresentar(self):
        print(f"Meu nome é {self.nome} e tenho {self.idade} anos.")

p1 = Pessoa("Ana", 22)
p1.apresentar()
```

### Decoradores
Decoradores são funções que modificam o comportamento de outras funções.

```python
def meu_decorator(func):
    def wrapper():
        print("Antes da função")
        func()
        print("Depois da função")
    return wrapper

@meu_decorator
def saudacao():
    print("Olá!")

saudacao()
```

### Geradores e Iteradores
Geradores facilitam a criação de iteradores.

```python
def contador():
    for i in range(5):
        yield i

for num in contador():
    print(num)
```

### Expressões Regulares
Expressões regulares permitem encontrar padrões em strings.

```python
import re
padrao = r"\d+"  # Encontra dígitos
resultado = re.findall(padrao, "Eu tenho 2 gatos e 3 cachorros.")
print(resultado)  # ['2', '3']
```

### Multithreading e Multiprocessing
Python oferece suporte a programação concorrente.

```python
import threading

def tarefa():
    print("Executando tarefa")

thread = threading.Thread(target=tarefa)
thread.start()
```

### Programação Assíncrona
Python possui bibliotecas para programação assíncrona como `asyncio`.

```python
import asyncio

async def main():
    print("Olá")
    await asyncio.sleep(1)
    print("Mundo")

asyncio.run(main())
```

### Metaprogramação
Metaprogramação permite modificar o comportamento de classes e funções em tempo de execução.

```python
def cria_classe():
    return type('NovaClasse', (object,), {})

MinhaClasse = cria_classe()
print(MinhaClasse)
```

### Testes Unitários e TDD
Os testes unitários garantem que seu código funcione conforme esperado.

```python
import unittest

def soma(a, b):
    return a + b

class TestSoma(unittest.TestCase):
    def test_soma(self):
        self.assertEqual(soma(2, 3), 5)

if __name__ == "__main__":
    unittest.main()
```

### Otimização de Código
Otimização envolve melhorar a performance do código.

```python
import time

start = time.time()

# Código a ser otimizado

end = time.time()
print(f"Tempo de execução: {end - start}")
```

### Integração com C/C++
Python pode ser integrado com C/C++ para otimização.

```c
# Código C embutido pode ser chamado por Python usando bibliotecas como ctypes.
```

## Hacking com Python

### Criando um Keylogger
### Criando seu RAT
### Criando seu WiFi Sniffer
### Criando seu Ransomware
### Criando seu Botnet
### Criando seu DDoS
### Mail Sniffer
### Git Trojan

## Hardware Hacking
### Introdução ao Hardware Hacking
### Raspberry Pi para Hacking
### Arduino para Hacking
### ESP32 e ESP8266

## Análise e Engenharia de Dados
### Introdução à Análise de Dados
### Pandas para Manipulação
### NumPy
### Visualização com Matplotlib
### Machine Learning Básico

## Versionamento
### Introdução ao Git
### Comandos Básicos do Git
### Branches e Merging

## Projeto do Zero: Backend e Frontend
### Planejamento e Arquitetura
### Backend com FastAPI
### Banco de Dados e ORM
### Autenticação e Autorização
### Frontend com React
### Integração Backend-Frontend
### Testes e Qualidade de Código
### Deployment e CI/CD
