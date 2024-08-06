O aluno Roger estava determinado a competir com seus colegas de classe para ver quem conseguia resolver mais rapidamente problemas de matemática. Para isso, ele se interessou em criar um programa que convertesse o tempo de cada um de minutos para segundos.

Isso poderia facilmente ser feito da seguinte maneira:

```jsx
tempo_segundos = tempo_minutos * 60
```

O código acima seria muito rápido de se escrever para uma competição entre _ e uma quantidade pequena de outros alunos. Por exemplo, supondo que temos: 

| Competidor | Tempo em Minutos |
| --- | --- |
| Roger | 2 |
| João | 3 |
| André | 5 |

```python
tempo_segundos_roger = 2 * 60
tempo_segundos_joao = 3 * 60
tempo_segundos_andre = 5 * 60
```

Claramente Roger seria o ganhador. Mas, vamos supor que a competição fosse feita entre 40 alunos; seria muito cansativo escrever esse código para cada um dos competidores, certo?

É por isso que temos as chamadas **funções!**

## Definição

As funções são blocos de código que resolvem um problema específico e que podem ser chamados toda vez que queremos resolver tal problema. 

## Estrutura de uma Função

Basicamente, uma função tem três partes principais:

- Nome
- Parâmetros
- Corpo e Retorno

### Nome

É propriamente dito: “nome” é a nomenclatura que você fornece para sua função. Esse nome é importante para quando você quiser chamar a função em outros momentos do seu código.

### Parâmetros

Um parâmetro é um valor que você passa para uma função para que ela possa usar esse valor em suas operações. Uma função pode ter vários parâmetros diferentes.

Por exemplo, para ajudar o aluno _ no seu programa, os parâmetros poderiam ser o nome do competidor (string) e o tempo em minutos.

### Corpo e Retorno

O corpo de uma função é onde realmente escrevemos o que queremos processar. É onde você escreve as instruções ou o código que a função executará quando for chamada.

Já o retorno é o resultado final do trabalho da função. Ou seja, é o que será retornado depois de todo o corpo da função ser processado.

Vale enfatizar que nem todas as funções exigem um retorno. Você pode criar uma função que realiza uma série de operações, mas que não retorne nada como valor.

## Criação

Criamos uma função em Python da seguinte maneira:

```python
def nomeDaFuncao(parametro1, parametro2, parametro3):
	corpoDaFuncao
	return _
```

## Escopo de Variáveis

Vamos supor que agora a competição da matemática vai acontecer entre toda a escola, e que haverá um ganhador para cada uma das salas. 

O programa que será criado por _ não pode comparar o tempo entre estudantes de salas diferentes. Isso é o que definimos como **escopo.**

Uma variável que é criada dentro do corpo de uma função é limitada apenas para aquela função, não podendo ser usada em outras áreas do código. Essa variável não é acessível fora da função, assim como você não pode comparar o tempo de um estudante da turma A com o estudante da turma B.

## Resolução do Problema

Pensando que o parâmetro da função seria:

- Um dicionário:
    - Nome_do_aluno: tempo_em_minutos

```python
def menor_tempo_em_segundos(dicionario):
    competidor_menor_tempo = None # inicialmente, ninguém é ganhador
    menor_tempo = float('inf')  # Define o menor tempo como infinito inicialmente
    for competidor, tempo_minutos in dicionario.items(): #loop para percorrer cada item do dicionário
        tempo_segundos = tempo_minutos * 60 # para cada tempo em minutos, ele converte para segundos
        if tempo_segundos < menor_tempo: # se esse valor calculado for menor que o valor que está na variável menor_tempo, então agora o menor_tempo é esse tempo_segundos
            menor_tempo = tempo_segundos # atribui o menor_tempo ao que foi calculado agora
            competidor_menor_tempo = competidor # atribui o nome do competidor de menor tempo
    return competidor_menor_tempo, menor_tempo # retorna o nome do competidor com menor tempo e o seu respectivo tempo em segundos.
```

A função `menor_tempo_em_segundos` recebe um **dicionário como parâmetro,** com competidores e seus tempos em minutos, identificando o competidor com o menor tempo. Inicialmente, define `menor_tempo` como infinito e percorre o dicionário, convertendo os tempos de minutos para segundos. Se encontrar um tempo menor, atualiza o menor tempo e o nome do competidor. No final, retorna o nome do competidor com o menor tempo e o tempo dele em segundos.