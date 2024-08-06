## O que são dicionários?

Assim como listas, é uma estrutura de dados em python que serve para armazenar valores. Entretanto, em um dicionário, cada **valor** está associado a uma **chave**, sendo esses armazenados em pares.
Trazendo para o mundo real, cada vez que queremos armazenar o nome de um novo aluno, o associamos a sua matrícula, ou seja, a matrícula em um dicionário seria a chave, enquanto o nome do aluno seria o valor associado aquela chave.

Em um dicionário do mundo real, temos uma coleção de palavras, no qual cada palavra possui um ou mais significados. A ideia é a mesma em dicionários em programação. As palavras são as chaves, enquanto os seus significados são os valores associados aquela palavra.

---

## Como criar um dicionário?

Para inicializar um dicionários, utilizamos chaves ( **`{ }`** ):

```python
dicionario = { }
```

Para passarmos os elementos, devemos informar a **chave** e o seu respectivo **valor**, separados por dois pontos ( **`:`** ):

```python
dicionario = {chave1: valor1, chave2: valor2,...}
```

### Chaves

Em listas, identificamos um elemento através do seu índice. Em um dicionário, o elemento é identificado através da sua **chave**. As chaves são únicas, e podem ser de qualquer tipo (String, Int, Float, etc).

### Valor

É a informação ou dado que está associada a uma chave. O valor pode ser de vários tipos, como uma String, um valor numérico, uma lista e até mesmo, um outro dicionário.

### Exemplo

Nessa tabela, está o nome e o número de alguns alunos que pretendem entrar no grupo de estudos de programação de Roger, Daiana e Nelson:

| Aluno | Número |
| --- | --- |
| Ernesto | 9485-1234 |
| Bonna | 8456-0987 |
| Rodrigo | 9856-0394 |
| Alice | 9984-0490 |
| Marcelo | 8790-3321 |

Podemos transformar a tabela acima em um dicionário da seguinte forma:

```python
contatos = {"Ernesto": "9485-1234", "Bonna": "8456-0987", "Rodrigo": "9856-0394", 
					"Alice": "9984-0490", "Marcelo": "8790-3321"}
```

No código acima, criamos o dicionário intitulado “contatos”. Para cada par chave-valor, existe uma chave do tipo String, sendo essa o nome, assim como um valor do tipo String, sendo o número do aluno associado aquela nome.

---

## Manipulando dados em um dicionário

Dicionário são mutáveis, sendo assim, é possível adicionar, remover ou modificar um elemento no mesmo. Abaixo, trabalharemos com as operações citadas anteriormente.

### Adicionando dados em um dicionário

Para adicionar novos valores em um dicionário, basta informar qual será a  sua chave, e em seguida o seu valor.

### Exemplo:

Vamos reutilizar o nosso dicionário “contatos”, criado anteriormente:

```python
contatos = {"Ernesto": "9485-1234", "Bonna": "8456-0987", "Rodrigo": "9856-0394", 
					"Alice": "9984-0490", "Marcelo": "8790-3321"}
```

Suponhamos que o colega de classe Daniell também topou participar do grupo de estudos de programação. Podemos adicionar o membro no dicionário da seguinte forma:

```python
contatos["Daniell"] = "9394-0512"
```

No código acima, adicionamos o aluno “Daniell” (chave) que possui o número “9394-0512” (valor) no nosso dicionário “contatos’.

O dicionário agora se encontra assim:

```python
contatos = {"Ernesto": "9485-1234", "Bonna": "8456-0987", "Rodrigo": "9856-0394", 
					"Alice": "9984-0490", "Marcelo": "8790-3321", "Daniell": "9394-0512"}
```

### Como acessar um valor em um dicionário?

Podemos acessar um valor indicando a sua chave dentro de colchetes ( [ ] ) da seguinte forma:

```python
dicionario["chave"]
```

### Exemplo

Roger precisa visualizar o número de Daniell para adicioná-lo ao grupo de estudos. Para isso, ele pode executar o seguinte trecho de código:

```python
print(conatos["Daniell"])
```

No código acima, imprimimos na tela o valor “9394-0512”, que está associado a chave “Daniell” no dicionário “contatos”.

### Modificando elementos em um dicionário

Como dito anteriormente, por ser uma estrutura mutável, um dicionário pode sofrer modificações nos valores já existentes no mesmo. Para modificar um valor, devemos passar a chave, seguido do seu novo valor:

```python
dicionario["chave_existente"] = "novo_valor"
```

### Exemplo

Daiana descobriu que Rodrigo trocou de número, e precisa atualizar o seu número no dicionário “contatos”:

```python
alunos["Rodrigo"] = "8895-6789"
```

No código acima, realizamos uma atualização no valor associado a chave “Rodrigo”, que deixou de ser "9856-0394" e agora será "8895-6789".
O dicionário agora se encontra assim:

```python
contatos = {"Ernesto": "9485-1234", "Bonna": "8456-0987", "Rodrigo": "8895-6789", 
					"Alice": "9984-0490", "Marcelo": "8790-3321", "Daniell": "9394-0512"}
```

### Removendo um valor de um dicionário

Por último, podemos remover valores de um dicionário através da palavra “del”, seguida da chave que contém o valor que queremos remover:

```python
del dicionario["chave"]
```

### Exemplo

Ernesto quebrou o celular, e ficará sem por um tempo. Com isso, precisaremos remover o número do nosso dicionário já que ele não está mais em uso:

```python
del contatos["Ernesto"]
```

No código acima, removemos a chave “Ernesto”, assim como o valor que estava associado a mesma ("9485-1234").

O dicionário agora se encontra assim:

```python
contatos = {"Bonna": "8456-0987", "Rodrigo": "8895-6789", "Alice": "9984-0490", 
							"Marcelo": "8790-3321", "Daniell": "9394-0512"}
```

---

## Dicionários aninhados

Como mencionado anteriormente, dicionários podem ser compostos por elementos de diversos tipos, incluindo, outros dicionários. Utilizamos dicionários aninhados quando queremos armazenas dados mais complexos.

A criação de um dicionário aninhado é bem parecida com a criação de um dicionário comum. Passamos a chave, e em seguida, passamos o novo dicionário, que também irá conter os pares chave-valor:

```python
dicionario_aninhado = {"dicionario1_chave": {"subchave1": "valor1", "subchave2":, "valor2"},
												"dicionario2_chave": {"subchave3": "valor3", "subchave4":, "valor4"}}
```

### Exemplo:

Aproveitando o dicionário “contatos”, vamos aprimora-lo para além do número do aluno, conter também a idade e a data de aniversário. Podemos fazer da seguinte forma:

```python
contatos_info = {"Ernesto": {"numero": "9485-1234", "idade": 16, "aniversario": "15/04"}, 
					"Bonna": {"numero": "8456-0987", "idade": 16, "aniversario": "21/11"}, 
					"Rodrigo": {"numero": "9856-0394", "idade": 17, "aniversario": "15/07"}, 
					"Alice": {"numero": "9984-0490", "idade": 17, "aniversario": "10/12"}, 
					"Marcelo": {"numero": "8790-3321", "idade": 18, "aniversario": "02/03"},
					"Daniell": {"numero": "9394-0512", "idade": 16, "aniversario": "05/12"}}
```

No código acima, criamos o dicionário “contatos_info”, que possui outros dicionários como elementos. Cada dicionário dentro de “contatos_info” possui o nome do aluno como chave, e seu valor, é um outro dicionário. Dentro desses dicionários, cada pessoa possui três chaves, sendo elas: número, idade e aniversário. 

---

## Exibindo dados de um dicionário

Podemos exibir dados de um dicionários através da estrutura de repetição **`for`**  e o comando **`.items`** da seguinte forma:

```python
dicionario = {"chave1": "valor1", "chave2": "valor2", "chave3": "valor3"}

for chave, valor in dicionario.items():
    print(f"{chave}: {valor}")
```

No código acima, percorremos o dicionário “dicionario”, e imprimimos na tela todos os pares chave-valor do mesmo. O comando **`.items`** é um método que nos retorna uma visualização dos pares chave-valor em um dicionário.

### Exibindo dados de um dicionário aninhado

Para exibir dados de um dicionário aninhado, devemos utilizar a estrutura de repetição **`for`** duas vezes. A primeira, para ter acesso a chave principal e ao valor associado a ela, e o segundo, para acessar as subchaves e os valores:

```python
dicionario_aninhado = {"chave1": {"subchave1": 'valor1', "subchave2": "valor2"},
                       "chave2": {"subchave3": "valor3", "subchave4": "valor4"}}

for chave, valor in dicionario_aninhado.items():
    print(chave)
    for subchave, valor_subchave in valor.items():
        print(f"{subchave}: {valor_subchave}")
```

No código acima, primeiro, acessamos os pares chave-valor do dicionário principal. Para cada chave, o dicionário (valor) associado a ela e percorre os pares chave-valor do mesmo.

---

## Erros em dicionários

Por último, iremos abordar dois erros comuns que podem acontecer quando estamos trabalhando com dicionários.

### Chaves duplicadas

Como dito anteriormente, as chaves em um dicionário são únicas, ou seja, não pode haver duas chaves iguais no dicionário.  Caso você tente adicionar uma chave repetida, mas com um valor diferente, o que vai acontecer é uma sobescrita no valor anterior. 

### Exemplo

Agora, voltaremos a utilizar o nosso dicionário “contatos”. Digamos que temos mais um aluno chamado Marcelo para adicionar no nosso dicionário:

```python
contatos = {"Bonna": "8456-0987", "Rodrigo": "9856-0394", 
					"Alice": "9984-0490", "Marcelo": "8790-3321", "Daniell": "9394-0512"}
```

Entretanto, já há um aluno cujo a chave do seu número é o nome “Marcelo”. Caso eu tente adicionar o novo aluno com o mesmo nome que o antigo, o que vai acontecer é que ele irá sobrescrever o valor associado a chave Marcelo que está no dicionário:

```python
contatos["Marcelo"] = "9393-2984"
```

Ao executar o código acima, o valor associado a chave “Marcelo”, que antes era "8790-3321", será substituído pelo novo que está sendo passado ("9393-2984").
Para resolver o problema, podemos inserir o novo Marcelo com o seu nome e sobrenome, para diferenciar os alunos:

```python
contatos["Marcelo Oliveira"] = "9393-2984"
```

Dessa forma, conseguiremos manter os dois alunos no dicionário, sem que haja sobrescrita de dados.

O dicionário agora se encontra assim:

```python
contatos = {"Bonna": "8456-0987", "Rodrigo": "9856-0394", "Alice": "9984-0490", 
							"Marcelo": "8790-3321", "Daniell": "9394-0512", "Marcelo Oliveira": 
							"9393-2984"}
```

### Acessando elementos que não estão no dicionário

Outro erro comum, é tentar acessar um elemento que, ou nunca esteve no dicionário, ou foi removido em algum momento. Caso você tente acessar, o Python irá retornar um erro, indicando que não encontrou o elemento.

### Exemplo

Roger acreditava que tinha o contato de Eliab na agenda, e então rodou o seguinte código para exibir o número do aluno:

```python
print(contatos["Eliab"])
```

Entretanto, ao executar o trecho de código acima, foi retornada a seguinte mensagem:

```python
Traceback (most recent call last):
  File "dicionarios.py", line 4, in <module>
    print(contatos["Eliab"])
          ~~~~~~~~^^^^^^^^^
KeyError: 'Eliab'
```

O erro indica que a chave “Eliab” não foi encontrada no dicionário, ou seja, o número do aluno Eliab ainda não estava no dicionário de contatos.

**Desafio:** Teste os seus conhecimentos e adicione o contato de Eliab no dicionário “contatos”. Você pode adicionar o número que quiser.

Para evitar o erro, você pode verificar se o elemento está no dicionário da seguinte forma:

```python
print("Chave" in dicionario)
```

O código acima irá mostrar “True” caso a chave passada esteja  no dicionário, e “False” caso não esteja.

---

## Exercícios

1. Escreva um programa que gere um dicionário, em que cada chave seja um caractere, e seu valor seja o número desse caractere encontrado em uma frase lida. Exemplo: O rato → { “O”:1, “r”:1, “a”:1, “t”:1, “o”:1}
    
    ```python
    frase = input("Digite uma frase para contar as letras:")
    d = {}
    for letra in frase:
    	if letra in d:
    		d[letra] = d[letra] + 1
    	else:
    		d[letra] = 1
    print(d)
    ```
    
2. Escreva um programa que gere um dicionário, em que cada chave seja um caractere, e seu valor seja o número desse caractere encontrado em uma frase lida. Exemplo: O rato → { “O”:1, “r”:1, “a”:1, “t”:1, “o”:1}
    
    ```python
    # Solução alternativa, usando o método get do dicionário
    frase = input("Digite uma frase para contar as letras:")
    d = {}
    for letra in frase:
    	# Se letra não existir no dicionário, retorna 0
    	# se existir, retorna o valor anterior
    	d[letra] = d.get(letra, 0) + 1
    print(d)
    ```
    
3. Escreva um programa que leia uma string e imprima quantas vezes cada caractere aparece nessa string.
String: TTAAC Resultado: T: 2x A: 2x C: 1x
    
    ```python
    sequencia = input("Digite a string: ")
    contador = {}
    
    for letra in sequencia:
    	contador[letra] = contador.get(letra, 0) + 1
    for chave, valor in contador.items():
    	print(f"{chave}: {valor}x")
    ```
    
4. Escreva uma função que, dada uma lista de dicionários representando transações bancárias, agrupe as transações pelo tipo e calcule o saldo total para cada tipo de transação.
    
    ```python
    
    def agrupar_transacoes_por_tipo(transacoes):
        resultado = {}
        for transacao in transacoes:
            tipo = transacao['tipo']
            valor = transacao['valor']
            if tipo not in resultado:
                resultado[tipo] = 0
            resultado[tipo] += valor
        return resultado
    
    # Exemplo de uso
    transacoes = [
        {'tipo': 'compra', 'valor': 100},
        {'tipo': 'venda', 'valor': 200},
        {'tipo': 'compra', 'valor': 50},
        {'tipo': 'venda', 'valor': 150}
    ]
    print(agrupar_transacoes_por_tipo(transacoes))  # {'compra': 150, 'venda': 350}
    
    ```
    
5. Escreva uma função que recebe um dicionário onde as chaves são nomes de alunos e os valores são listas de notas. A função deve retornar um dicionário com os alunos e suas médias.
    
    ```python
    
    def calcular_media_alunos(alunos):
        return {aluno: sum(notas) / len(notas) for aluno, notas in alunos.items()}
    
    # Exemplo de uso
    alunos = {
        'Alice': [85, 92, 78],
        'Bob': [75, 85, 89],
        'Carlos': [90, 88, 95]
    }
    print(calcular_media_alunos(alunos))  # {'Alice': 85.0, 'Bob': 83.0, 'Carlos': 91.0}
    
    ```
    
6. Escreva uma função que recebe um dicionário e retorna um novo dicionário onde as chaves são os valores únicos do dicionário original e os valores são listas de chaves que correspondiam a esses valores.
    
    ```python
    def inverter_dicionario_para_lista(dicionario):
        invertido = {}
        for chave, valor in dicionario.items():
            if valor not in invertido:
                invertido[valor] = []
            invertido[valor].append(chave)
        return invertido
    
    # Exemplo de uso
    dicionario = {'a': 1, 'b': 2, 'c': 1}
    print(inverter_dicionario_para_lista(dicionario))  # {1: ['a', 'c'], 2: ['b']}
    
    ```
    
7. Dado um dicionário que representa um grafo (onde as chaves são nós e os valores são listas de vizinhos), escreva uma função para encontrar todos os caminhos possíveis entre dois nós.
    
    ```python
    
    def encontrar_todos_os_caminhos(grafo, inicio, fim, caminho=[]):
        caminho = caminho + [inicio]
        if inicio == fim:
            return [caminho]
        if inicio not in grafo:
            return []
        caminhos = []
        for no in grafo[inicio]:
            if no not in caminho:
                novos_caminhos = encontrar_todos_os_caminhos(grafo, no, fim, caminho)
                for novo_caminho in novos_caminhos:
                    caminhos.append(novo_caminho)
        return caminhos
    
    # Exemplo de uso
    grafo = {
        'A': ['B', 'C'],
        'B': ['C', 'D'],
        'C': ['D'],
        'D': ['C'],
        'E': ['F'],
        'F': ['C']
    }
    print(encontrar_todos_os_caminhos(grafo, 'A', 'D'))  # [['A', 'B', 'D'], ['A', 'B', 'C', 'D'], ['A', 'C', 'D']]
    
    ```
    
8. Escreva uma função que recebe um dicionário e uma função de filtro. A função deve retornar um novo dicionário contendo apenas os itens que satisfazem a função de filtro.
    
    ```python
    def filtrar_dicionario_com_funcao(dicionario, funcao_filtro):
        return {k: v for k, v in dicionario.items() if funcao_filtro(k, v)}
    
    # Exemplo de uso
    dicionario = {'a': 1, 'b': 3, 'c': 2}
    funcao_filtro = lambda k, v: v > 1
    print(filtrar_dicionario_com_funcao(dicionario, funcao_filtro))  # {'b': 3, 'c': 2}
    
    ```
    
9. Escreva uma função que recebe uma lista de dicionários representando pedidos de um e-commerce (cada dicionário tem 'produto', 'preço', 'quantidade') e retorna um dicionário com o faturamento total por produto.
    
    ```python
    def calcular_faturamento_pedidos(pedidos):
        faturamento = {}
        for pedido in pedidos:
            produto = pedido['produto']
            total = pedido['preço'] * pedido['quantidade']
            if produto in faturamento:
                faturamento[produto] += total
            else:
                faturamento[produto] = total
        return faturamento
    
    # Exemplo de uso
    pedidos = [
        {'produto': 'A', 'preço': 10, 'quantidade': 2},
        {'produto': 'B', 'preço': 5, 'quantidade': 5},
        {'produto': 'A', 'preço': 10, 'quantidade': 1}
    ]
    print(calcular_faturamento_pedidos(pedidos))  # {'A': 30, 'B': 25}
    
    ```
    
10. Escreva uma função que recebe uma lista de dicionários representando alunos e suas notas em diferentes disciplinas e retorna um dicionário com a média das notas por disciplina.
    
    ```python
    def media_notas_por_disciplina(alunos):
        disciplinas = {}
        for aluno in alunos:
            for disciplina, nota in aluno['notas'].items():
                if disciplina not in disciplinas:
                    disciplinas[disciplina] = []
                disciplinas[disciplina].append(nota)
        return {disciplina: sum(notas) / len(notas) for disciplina, notas in disciplinas.items()}
    
    # Exemplo de uso
    alunos = [
        {'nome': 'Alice', 'notas': {'matemática': 90, 'história': 85, 'ciências': 92}},
        {'nome': 'Bob', 'notas': {'matemática': 88, 'história': 79, 'ciências': 95}},
        {'nome': 'Carlos', 'notas': {'matemática': 92, 'história': 87, 'ciências': 90}}
    ]
    print(media_notas_por_disciplina(alunos))  # {'matemática': 90.0, 'história': 83.66666666666667, 'ciências': 92.33333333333333}
    
    ```
    
11. Escreva uma função que recebe uma lista de dicionários representando produtos e retorna o produto mais caro e o mais barato.
    
    ```python
    def produto_mais_caro_e_barato(produtos):
        mais_caro = max(produtos, key=lambda x: x['preço'])
        mais_barato = min(produtos, key=lambda x: x['preço'])
        return mais_caro, mais_barato
    
    # Exemplo de uso
    produtos = [
        {'nome': 'Produto A', 'preço': 10},
        {'nome': 'Produto B', 'preço': 5},
        {'nome': 'Produto C', 'preço': 15}
    ]
    print(produto_mais_caro_e_barato(produtos))  # ({'nome': 'Produto C', 'preço': 15}, {'nome': 'Produto B', 'preço': 5})
    
    ```
    
12. Escreva uma função que recebe uma lista de dicionários representando pessoas (com nome, idade, cidade) e retorna um dicionário agrupando as pessoas por cidade.

```python
def agrupar_por_cidade(pessoas):
    cidades = {}
    for pessoa in pessoas:
        cidade = pessoa['cidade']
        if cidade not in cidades:
            cidades[cidade] = []
        cidades[cidade].append(pessoa)
    return cidades

# Exemplo de uso
pessoas = [
    {'nome': 'Alice', 'idade': 30, 'cidade': 'São Paulo'},
    {'nome': 'Bob', 'idade': 25, 'cidade': 'Rio de Janeiro'},
    {'nome': 'Carlos', 'idade': 35, 'cidade': 'São Paulo'}
]
print(agrupar_por_cidade(pessoas))  # {'São Paulo': [{'nome': 'Alice', 'idade': 30}, {'nome': 'Carlos', 'idade': 35}], 'Rio de Janeiro': [{'nome': 'Bob', 'idade': 25}]}


```