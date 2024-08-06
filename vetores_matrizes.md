# Vetores

Nelson está atribuindo as notas aos seus alunos utilizando a lista da chamada. Naturalmente, ele irá corrigir as provas na ordem em que os alunos aparecem na chamada e atribuir suas notas. Dito isso, como Nelson está aprendendo programação, tentará implementar um código para facilitar sua correção. Mas, como representar as notas dos seus alunos?

### Como inicializar listas?

As listas são estruturas de dados que contém elementos do mesmo tipo ou não que são alocados de forma ordenada no seu programa. A atribuição de uma lista é feita através de colchetes ([]), por exemplo:

```python
notas_alunos = [10, 6, 7, 7, 5, 9]
```

### Como revelar cada elemento de uma lista?

Cada elemento da lista tem um número associado a ele chamado **índice** que sempre é iniciado com 0. Por exemplo, em notas_alunos o elemento “10” está na posição 0 e o elemento “5” está na posição 4. Para acessar cada posição da lista, escreve-se o nome da lista com o índice entre colchetes, como:

```python
notas_alunos[1] #retorna 6
```

### Como ler e printar cada elemento da lista?

Dessa forma, para ler e printar cada elemento da lista, é preciso iterar sobre o índice até o fim da lista. Para fazer isso, é comum utilizar os laços de repetição em conjunto com duas funções: **`len()`** e **`range()`**. A função **`len()`** retorna o tamanho em formato inteiro da lista que é passada para ela entre parêntesis e a função **`range()`** retorna um intervalo do primeiro índice da lista (0) até o último (5), por exemplo:

```python
for i in range(len(notas_alunos)):
	print(notas_alunos[i]) #printa cada nota inserida em notas_alunos
```

### Como modificar a lista?

Outra possibilidade para as listas é modificar um valor específico dentro dela. Para fazer isso, escreve-se o nome da variável referente à lista com o índice do elemento que deseja modificar e um operador de atribuição. Por exemplo:

```python
notas_alunos[1] = 7 #Modifica o elemento de índice 1 da lista (6) para o valor 7
```

# Funções

## append()

Para incluir elementos em uma lista, recomenda-se utilizar uma função nativa das listas que é o append(). Essa função recebe como parâmetro o elemento que você deseja adicionar na lista dentro de seus parêntesis e o adiciona no **fim da lista**. Uma boa analogia para esse caso seria o ato de adicionar um novo livro a uma prateleira que já tem alguns livros guardados. Para implementar o append(), escreve-se:

```python
lista.append('novo elemento')
```

## remove()

Quando falamos de listas, além de saber como adicionar elementos, é relevante ter conhecimento de como retirar elementos. Para auxiliar nisso, a função remove() recebe como parâmetro o elemento a ser retirado e realiza sua remoção da lista. Por exemplo:

```python
lista_de_presentes = ['boneco', 'skate', 'bike']

print(lista_de_presentes) #['boneco', 'skate', 'bike']

lista_de_presentes.remove('boneco')

print(lista_de_presentes) #['skate', 'bike']
```

## index()

Eventualmente, pode ser relevante saber a posição em que um elemento da lista está ocupando. Para isso, existe a função de listas index() a qual recebe como parâmetro um elemento que está dentro da lista e retorna a posição em que ele se encontra, por exemplo:

```python
alunos = ['cláudia', 'ione', 'maria']
alunos.index('ione') #retorna o valor 1
```

## pop()

A função pop() faz o último elemento da lista “pular” para fora dela e retorna esse mesmo elemento no local onde foi chamada. Por exemplo:

```python
carros = ['logan', 'mobi', 'celta']
print(carros.pop()) #irá printar 'celta' e o removerá da lista
```

# Strings

Strings nada mais são que listas de caracteres encadeados, podendo armazenar textos, palavras, nomes e frases. Em Python, as Strings são tratadas como um tipo de variável, ou seja, podem ser envolvidas em *castings como:*

 

```python
altura = 1.68
texto_altura = str(altura) #Atribui a altura (float) convertida para string em texto_altura
```

Além disso, as Strings podem ser tratadas como listas também, inclusive, herdando algumas funções desse tipo como append() e index(). Por exemplo:

```python
nome_completo = 'Maria Auxiliadora'
print(nome_completo[0]) #Irá printar a primeira letra do nome completo ('M')
```

No entanto, não é possível realizar operações de atribuição envolvendo os índices da String após sua criação, como:

```python
nome_completo = 'Marco Aurélio'
nome_completo[0] = 'A' #Retorna um erro, pois as Strings são imutáveis
```

## Operações com Strings

### Concatenação

Roger está pensando em fazer um código para uma calculadora simples das 4 operações (+, -, /, *). Ao printar o resultado, Roger deseja colocar uma mensagem amigável para o usuário contendo o resultado do cálculo. Mas, como ele poderia fazer isso?

O conteúdo de duas ou mais Strings pode ser juntado ou concatenado através do operador de concatenação (+). Resolvendo o exemplo acima, temos:

```python
resultado = 20

print("O resultado é" + str(resultado)) #Concatena a primeira String com a conversão de resultado (int) para String
```

Um caso particular de concatenação é utilizando o operador de multiplicação (*) como:

```python
print('A' * 3) #Printa a mesma String repetida 3 vezes ('AAA')
```

### Composição

Além de realizar o *casting*, as Strings contam com uma ferramenta muito interessante chamada composição. Essa ferramenta funciona da seguinte forma:

1. Declaramos onde e quais os tipos das variáveis que serão incluídas na composição segundo a tabela:
    
    ![marcadores-comp-string-python.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/626cfd9d-491d-4969-8427-bf527f4f855d/debd0cb1-43ba-4a60-9cb6-0a5c59153696/marcadores-comp-string-python.png)
    
2. Separamos os marcadores das variáveis pelo operador ‘%’
3. Definimos as variáveis que serão incluídas em ordem.

No exemplo da calculadora de Roger, podemos implementar um output que informe os números passados e o seu resultado da seguinte forma:

```python
x = 2
y = 4
resultado = 2 + 4

print("%d + %d = %d" % (x, y, resultado)) #Printa "2 + 4 = 6"
```

Outra aplicação da composição é a formatação de casas decimais do tipo float. Por exemplo:

```python
print("O resultado é: %.2f" % 3.567) #Printa: "O resultado é: 3.57"
```

Uma outra alternativa à composição, é utilizar o print(f’’) que permite adicionar as variáveis “dentro” da String, como:

```python
resultado = 24
print(f"O resultado é: {resultado}") #Printa: "O resultado é: 24"
```

### Slicing

É possível fatiar strings de modo a utilizar somente uma parte dela. Para isso, escreve-se o nome da variável que contém a String com um colchetes ([]) indicando os índices de início e fim do fatiamento. Por exemplo:

```python
fim_jogo = "Flamengo venceu o Vasco"
vencedor = fim_jogo[0:8] #Da posição 0 até a posição 8 ("Flamengo")
perdedor = fim_jogo[17:23] #Da posição 17 até a posição 23 ("Vasco")
```

O conteúdo dos colchetes é:

1. Índice de início do fatiamento (0 e 17 no exemplo)
2. O símbolo de dois pontos (:) representando “até”
3. Índice do fim do fatiamento não inclusivo. Ou seja, se o último caractere desejado está na posição 22, o índice do fim do fatiamento não inclusivo é 23.

Obs 1: É possível omitir o ínicio e o fim da string. Ou seja, ao invés de ter colocado [0:8] e [17:23] no exemplo anterior, poderia colocar somente [:8] e [17:].

Obs 2: É possível representar o último caractere da string como -1, o penúltimo por -2, o antepenúltimo por -3 e assim por diante. Por exemplo:

```python
encontre_erro = "Famint%"

erro = encontre_erro[-1:] #Retorna e atribui "%" para erro

print(f"O erro está em {erro}") #Printa: "O erro está em %"
```

## Funções de String

### Verificação parcial de Strings

Para verificar se uma string termina ou começa com alguns caracteres, utiliza-se as funções **endswith** e **startswith**, respectivamente. Essas funções retornam um valor booleano (True ou False) de acordo com a string que deseja se analisar. Por exemplo:

```python
mensagem = "João vem amanhã?"

print(mensagem.startswith("João")) #Retorno será True
print(mensagem.endswith("hoje")) #Retorno será False
```

Algo que pode ser questionado nesse tipo de problema é: “Como analisar strings independemente de ter letras maiúsculas ou minúsculas?”. A resposta é que é possível converter toda a string para ter somente letras maiúsculas ou somente letras minúsculas com as funções upper() e lower(). Essas duas funções retornam a string somente com letras maiúsculas ou minúsculas, mas não transforma a string logo quando é chamada. Ou seja, é preciso atribuir o retorno dessas funções à variável que contém a string. Veja o exemplo:

```python
nome = "João SiLvA"
print(nome.endswith("silva")) #Retorna False

nome = nome.lower()
print(nome.endswith("silva")) #Retorna True
```

Repare que, até agora, só foi explicado como realizar a verificação de uma cadeia de caracteres. No entanto, é possível que o problema peça para que você verifique se há somente um caractere presente na string em qualquer posição dela, certo? Nesse caso, o comando ‘in’ é bastante competente, pois ele verifica se um ou mais caracteres estão presentes na string em qualquer posição. Além disso, é possível negar o ‘in’ caso seja necessário verificar se aquele(s) caractere(s) não estão na string com o comando ‘not’. Vejamos sua implementação:

```python
frase = "Iara virá hoje para a aula"

print("I" in frase) #Retorna True
print("hoje" in frase) #Retorna True
print("vem" in frase) #Retorna False

print("w" not in frase) #Retorna True
print("para" not in frase) #Retorna False
```

### Contagem

Quando é necessário contar o número de ocorrências de um ou mais caracteres em uma string, usa-se a função count, a qual retorna um número inteiro que representa essa quantidade de repetições. Veja o exemplo:

```python
mensagem_carinhosa = "Maria é tudo para mim, tudo o que eu poderia querer e tudo o que eu poderia ter"

print(mensagem_carinhosa.count("tudo")) #Retorna 3
print(mensagem_carinhosa.count("poderia")) #Retorna 2
```

### Pesquisa

Tradicionalmente, sempre que é preciso encontrar o íncide de algum caractere específico na string, usa se um laço de repetição para varrer toda a lista. No entanto, existem alternativas para isso que deixam o código bem mais legível e organizado: a funções **find()**. A função find() realiza uma busca na string da **esquerda para a direita** e retorna o índice da primeira ocorrência do caractere passado no seu parâmetro caso esteja presente, **caso não esteja retorna -1**. Vale salientar que, quando mais de um caractere é passado, essa função retorna a primeira posição da primeira ocorrência desse conjunto. Por exemplo:

```python
frase_motivacional = "Desapegue do medo, desafie seus limites e desbrave novos horizontes!"

print(frase_motivacional.find('a')) #Retorna 3
print(frase_motivacional.find('des')) #Retorna 0
```

Além disso, a função find também aceita mais dois parâmetros: **início** e **fim** da busca. Por exemplo:

```python
frase_motivacional = "Desapegue do medo, desafie seus limites e desbrave novos horizontes!"

print(frase_motivacional.find('a', 2, 15)) #Retorna 3
print(frase_motivacional.find('des', 5, 20)) #Retorna -1
```

### Comparação

Para comparar duas strings, usam-se os mesmos operadores de comparação (<, ≤, >, ≥, ==), porém com significados distintos. Para os comparadores < e >, compara-se pela ordem alfabética das duas strings. Por exemplo:

```python
marca1 = "weg"
marca2 = "logica"

print(marca1 > marca2) #Retorna True
```

Para o operador de ==, verifica se uma string é exatamente igual à outra.

### replace()

Em python, é possível substituir todas as ocorrências de uma substring na string maior por algum outro valor que se queira. Para isso, usa-se a função replace() que suporta dois parâmetros: a substring e a string de substituição. Veja o exemplo:

```python
mensagem = "Hoje está um dia ensolarado, mas pode chover mais tarde."

nova_string = mensagem.replace("ensolarado", "chuvoso")

print(nova_string) #Hoje está um dia chuvoso, mas pode chover mais tarde.
```

# Matrizes

Roger e Diana estavam no intervalo das suas aulas e decidiram jogar um jogo de tabuleiro juntos na cantina da escola. O jogo escolhido por eles foi o Batalha Naval*, porém eles estavam sem um tabuleiro. Então, Roger lembra a Diana que eles estão estudando programação e seria muito legal programar um jogo como esse no computador. Mas como representar o tabuleiro?

### Como inicializar matrizes?

Matrizes são estruturas de dados que contém linha e coluna, sendo, basicamente, tratadas como “listas de listas”. Ou seja, a matriz é uma lista que contém outras listas dentro dela. Devido a essa característica, essa estrutura é muito utilizada quando precisa-se representar tabuleiros. Dito isso, vamos implementar o exemplo citado acima, representando ‘B’ como barco, ‘F’ como auto-destruição e ‘A’ como água:

```python
#Primeira forma de inicializar Matrizes

linha0 = ['A', 'B', 'F', 'B', 'B']
linha1 = ['B', 'A', 'A', 'B', 'F']
linha2 = ['F', 'B', 'B', 'B', 'B']
linha3 = ['A', 'B', 'F', 'A', 'B']
linha4 = ['B', 'F', 'A', 'B', 'F']

tabuleiro = [linha0, linha1, linha2, linha3, linha4] #Matriz 5x5 que representa o tabuleiro do jogo
```

Outra forma de criar matrizes é escrevendo o conteúdo das linhas diretamente na sua atribuição. No exemplo acima, o código seria:

```python
#Segunda forma de inicializar Matrizes
tabuleiro = [
    ['A', 'B', 'F', 'B', 'B'],
    ['B', 'A', 'A', 'B', 'F'],
    ['F', 'B', 'B', 'B', 'B'],
    ['A', 'B', 'F', 'A', 'B'],
    ['B', 'F', 'A', 'B', 'F']
]
```

### Como acessar elementos da matriz?

Assim como na Batalha Naval, cada elemento da matriz é acessado pelo número da sua linha e sua coluna que, assim como em listas, são representados por colchetes (’[]’) juntos ao nome da matriz. Por exemplo:

```python
print(tabuleiro[0][1]) #Retorna 'B' que está na linha 0 e coluna 1
```

### Como ler os elementos da matriz?

Dessa forma, é preciso utilizar dois loops para ler cada elemento da matriz: um loop para varrer as linhas e outro loop para varrer as colunas. Essa interpretação pode não ser trivial, portanto, atente ao passo a passo:

1. **Lendo cada linha**

Como a linha representa uma lista dentro da matriz, naturalmente, precisamos iterar sobre ela para podermos acessar cada uma. Assim, codifica-se da seguinte forma:

```python
for linha in range(len(tabuleiro)):
	print(tabuleiro[linha]) #Retorna cada linha do tabuleiro
```

1. **Lendo cada coluna**

Já que nós conseguimos revelar cada linha da matriz com o for, agora precisamos saber o que há nas linhas, ou seja, as colunas da matriz. Desse modo, precisamos iterar sobre cada linha para revelar os elementos das colunas. Dito isso, o código ficaria:

```python
for linha in range(len(tabuleiro)): #itera sobre a matriz como um todo
	for coluna in range(len(tabuleiro[linha])): #itera sobre cada linha da matriz
		print(tabuleiro[linha][coluna]) #Retorna cada elemento das colunas da matriz, uma linha de cada vez
```

### Como modificar matrizes?

Como o tratamento de matrizes é bastante parecido com o tratamento de listas, a modificação de elementos da matriz segue as mesmas regras da lista. Assim, o código é:

```python
tabuleiro[2][2] = 'A' #Modifica o elemento na linha 2 e coluna 2 ('B') para 'A'
```

## Questões propostas