## Problemática

Nelson passou uma atividade de programação onde ele queria que os alunos criassem um código que imprimisse uma sequência de números, mas para isso eles não poderiam escrever **`print`** várias vezes. Vamos descobrir agora como podemos ajudar os alunos de Nelson nessa atividade utilizando algo chamado **repetição.**

## Definição

- Os loops ou estruturas de repetições são estruturas que um código pode ser executado mais de uma vez, é muito útil para dar uma mobilidade maior para o código, evitando, por exemplo, repetir a mesma estrutura para algo que seja igual. Há duas formas de fazer em python, **`while`** e **`for`**. Embora seja essencial para a programação, é preciso ter cuidado para encerrar os loops para que o código possa ser finalizado quando necessário.

## While

- O **`while`** é usado para repetir um bloco de código enquanto tivermos uma condição que seja verdadeira. Por exemplo: se eu quiser imprimir uma sequência de números de 0 a 10, eu não preciso usar diversas vezes o **`print`,** eu posso resolver isso utilizando um laço de repetição.

```python
contador = 0
while contador <= 10:
    print(contador)
    contador += 1

```

- No exemplo acima temos um laço que vai imprimir números de 0 a 10, para que isso aconteça temos um **contador** que nada mais é do que o que define a condição do laço **`while`**. Cada vez que o laço é rodado, o contador soma mais **1**, quando o laço rodar com o contador em 10 ele vai imprimir o número 10 e somar mais 1 ao contador ficando com **11**, quando ele for passar pelo laço novamente, não será aceito já que nossa condição inicial era de que o **contador** seria **menor ou igual** a 10. Dessa forma o laço vai parar de rodar e teremos os números desejados impressos.

### Break

- O **`break`** é uma forma de sair do laço, evitando que ele se torne infinito.

```python
contador = 0
while True:
    print(contador)
    contador += 1
    if contador > 10:
        break

```

- No exemplo acima temos o mesmo contador, a diferença nesse caso está na condição do laço que agora é true, enquanto o laço for verdadeiro ele vai continuar rodando.  Logo abaixo temos um **`if contador > 10`**, ele vai verificar se o contador é maior que 10, caso seja, o **`break`** é ativado fazendo com que o laço encerre.

### Continue

- O continue faz com que o laço pule para uma próxima interação quando ocorre uma determinada condição.

```python
contador = 0
while contador < 5:
    contador += 1
    if contador == 3:
        continue
    print(contador)

```

- No exemplo temos que o laço vai imprimir os valores até **5**, uma vez que a condição do laço impõe isso, no entanto, existe um **`if`** no meio com a condição de que se o contador for igual a **3** ele deve acionar o **`continue`**, dessa forma ele irá pular o print sem imprimir o valor **3**, e começara o loop imprimindo novamente os demais números. Ao final teremos a saída **0, 1, 2, 4, 5.**

### Laço infinito

- O laço infinito ocorre quando não definimos exatamente qual a condição de parada

```python
contador = 0
while contador < 5:
    print(contador)

```

- No exemplo temos quase o mesmo código dos demais exemplos, entretanto, neste código o contador não está sendo acrescentado 1, logo temos que esse contador sempre será igual a zero, dessa forma, o laço vai se estender infinitamente imprimindo o valor 0.

## For

- O laço **`for`** é utilizado para passar pelos elementos de uma sequência (como uma lista, tupla, dicionário, string, etc.) essas serão vistas mais a frente. O **`for`** é utilizado também para iterar sobre uma sequência de números

### Range

- O range é uma função python que gera uma sequência de números, onde o laço pode iterar sobre essa sequência.

```python
print("Contagem de notas:")
for nota in range(1, 6):
    print(f"Nota {nota}")

```

- Nesse exemplo temos que o laço for vai iterar sobre a sequência definida no **`range`**, esse **`range`** ira gerar uma sequência de **1 a 5**, nesse caso do **`range`** ele para a sequência **um número antes**, por isso que vai até **5**.

### 

### Iterando lista

- Iterar sobre lista com o for é quando o laço consegue passar por cada elemento de uma lista e realizar algo com ele.

```python

# Lista de tópicos sobre programação
topicos_ti = ["Variáveis", "Estruturas de Controle", "Funções", "Listas", "Dicionários"]

# Iterando sobre a lista e imprimindo os tópicos
print("Tópicos sobre Programação:")
for topico in topicos_ti:
    print(topico)

```

- Nesse exemplo simples temos uma lista com assuntos de programação e desejamos imprimir os elementos dessa lista, para isso podemos utilizar o laço **`for`**, ele vai passar por cada um dos elementos da lista e em seguida imprime cada um.

## Exercícios

### Exercício 1

- Roger e Diana precisam criam um código que leia um número inteiro e diga se esse número é primo ou não. Eles aprenderam nas aulas do professor Nelson que um número é primo se ele for divisível por 1 e por si. Portanto, o resto da divisão é 0. Com base nos seus conhecimentos em Python até aqui, faça um código que recebe um número inteiro como entrada e devolve uma string dizendo se o número é primo ou não.
- Entrada: 5
- Saida: 5 é um número primo!
- Entrada: 6
- Saida: 6 Não é um número primo!

```python
#Resposta

n = int(input('Digite um número natural: '))
divisores = 0

# Verificando o número de divisores de n entre {1..n}
for i in range(1, n + 1):
    if n % i == 0:
        divisores += 1

if divisores == 2:
    print(f'{n} é um número primo')
else:
    print(f'{n} NÃO é um número primo')

```

### Exercício 2

Nelson corrigiu as provas de seus alunos e agora ele gostaria de saber qual foi a maior nota, a menor e media das notas de seus alunos. Para isso, ele conta com sua ajuda para construir um programa que recebe um número inteiro que identifica quantas notas serão colocadas, depois uma entrada contendo as notas dos alunos, e por fim será impresso qual foi a menor nota, a maior e a média das notas. 

```python
#Resposta

n = int(input('Quantas notas serão consideradas? '))
soma_notas = 0
menor_nota = 0
maior_nota = 0

for i in range(n):
    nota = float(input(f'Digite a nota do aluno {i+1}: '))
    soma_notas += nota
    
    if nota < menor_nota or i == 0:  # Atualiza a menor nota se for a primeira nota ou se a nota atual for menor
        menor_nota = nota
    if nota > maior_nota or i == 0:  # Atualiza a maior nota se for a primeira nota ou se a nota atual for maior
        maior_nota = nota

media_notas = soma_notas / n

print()
print(f'Menor nota: {menor_nota:.2f}')
print(f'Nota média da turma: {media_notas:.2f}')
print(f'Maior nota: {maior_nota:.2f}')

```

### Exercícios

1. Faça um programa que leia um nome de usuário e a sua senha e não aceite a senha igual ao nome do usuário, mostrando uma mensagem de erro e voltando a pedir as informações.
2.  Faça um programa, utilizando **`*while*`**, que mostre na tela de 0 até N, em que N é o limite inserido pelo usuário.
3.  Faça um programa, utilizando ***while***, que permita o usuário fazer contas de adição enquanto quiser.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/626cfd9d-491d-4969-8427-bf527f4f855d/54eb4a0b-f91a-4d59-9536-e314b9bac281/Untitled.png)

1. Faça um programa que imprime a quantidade de números pares de 100 até 200, incluindo-os.
2. Faça um programa para escrever a contagem regressiva do lança-
mento de um foguete. O programa deve imprimir 10, 9, 8, ... , 1, O e Fogo! na tela.
3. Escreva um programa que leia dois números. Imprima o resultado da multiplicação do primeiro pelo segundo. Utilize apenas os operadores de soma e subtração para calcular o resultado. Lembre-se de que podemos entender a multi-plicação de dois números como somas sucessivas de um deles. Assim, 4 x 5 = 5 +5 + 5 + 5 = 4 + 4 + 4 + 4 + 4.
4. Exibir o total da soma obtida dos cem primeiros números inteiros utilizando FOR.
5. Exibir a série de Fibonacci até o termo N especificado pelo usuário (N>9) através do teclado. A série de Fibonacci é formada pela sequência: 1, 1, 2, 3, 5, 8, 13, 21, 34, ... , etc. Esta série se caracteriza por seu próximo termo ser obtido da soma dos dois últimos termos da série.