### Apresentação

Bem vindo a apostila de conteúdos do conecta pet, uma atividade desenvolvida pelo grupo pet informática da UFPE.

Nessa apostila você vai encontrar conteúdos e exercícios essenciais para poder se preparar para a certificação do conecta pet. 

Recomendações:

- Acompanhe todas as etapas desta apostila para ter a melhor experiência possível, pular etapas pode ser muito prejudicial, principalmente para iniciantes.
- Pratique o máximo que puder, está é a única forma de aprender lógica e uma nova linguagem de programação.
- Estude lógica de programação esse conteúdo é a base para fundamental para todo programador conseguir desenvolver suas soluções e resolver os problemas no mundo real.
- Estude mais sobre abstração da realidade e pensamento computacional esse conteúdo vai permitir que você consiga pensar de forma mais elaborada, organizada e eficiente as soluções para os problemas que serão propostos para você, além de ser extremamente importante para poder conseguir entender como trazer as situações da realidade para o mundo do desenvolvimento de software e conseguir resolver através da tecnologia.

Além disso recomendamos que você procure outros exercícios para se preparar para a certificação, ao final de cada conteúdo você encontrará uma lista de exercícios sugeridos para poder aprimorar ainda mais seus conhecimentos sobre aquele assunto e ficar pronto para a certificação do conecta.pet. Lembre-se, é extremamente importante que você faça os exercícios para poder aprimorar seus conhecimentos e conseguir a certificação.

### Algoritmo

A primeira coisa que você deve compreender para iniciar essa jornada é o conceito de algoritmo. O conceito é simples e pode ser descrito da seguinte maneira:

“Um algoritmo é uma sequência de ações a serem realizadas para cumprir uma tarefa”

Tendo em mente esta definição, agora, você precisa saber que tudo o que programadores fazem, são algoritmos. Programação é apenas “dizer” ao computador como realizar uma tarefa. Para fazer isto.

Para entender melhor o que é um algoritmo, você pode pensar em algumas atividades cotidianas, por exemplo, cozinhar. Uma receita é um ótimo exemplo, pois é exatamente um algoritmo para quem quer fazer um bolo, explicando passo a passo o que precisa ser feito, com um computador funciona da mesma forma. 

### Linguagens de programação

As linguagens de programação são as ferramentas que simplificam a comunicação entre humano e computador, é através delas que os algoritmos podem ser escritos. Cada linguagem possui um conjunto de instruções que podem ser compreendidas pelo computador. É com estas palavras reservadas que conseguimos escrever a lógica de um algoritmo de forma que possa ser processada e executada por um computador. Existem diversas linguagens, nesta apostila serão apresentados os fundamentos da linguagem python.  Cada linguagem de programação tem palavras, regras e funções diferentes, o que há de comum entre todas é a lógica, por isso este também será o nosso foco de ensino, pois ao compreender as estruturas de controle de fluxo e aprender a utiliza-las, será capaz de aprender uma nova linguagem com facilidade.

### Entrada, processamento de dados e saída

Antes de por a mão na massa, há mais uma coisa que você deve entender. Para conhecer o funcionamento de um programa é muito comum começar por uma abstração do que ele faz, ao invés de olhar diretamente para o código que ele executa, é melhor vê-lo funcionando, ou pensar em seu funcionamento antes de implementa-lo. Para conseguir fazer isto utilizamos sempre os conceitos de entrada, processamento e saída da seguinte forma:

Entrada: Valores necessários para a execução do programa.

Processamento: A execução do programa.

Saída: O resultado do que o programa executou.

O exemplo mais simples para entender isso é pensar no programa como uma caixa preta, onde você pode inserir algumas coisas fecha-la e quando abrir novamente, terão coisa diferentes lá. Isto nos ajuda a pensar em como planejar a maneira que nosso algoritmo deve funcionar.

Na imagem a baixo temos um exemplo de como funciona um algoritmo que exibe o nome de um usuário, recebendo como entrada o nome dele.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/626cfd9d-491d-4969-8427-bf527f4f855d/951212d4-9577-4410-9b9d-97d1b0a6550a/Untitled.png)

### Variáveis

Após entender o que é um algoritmo, você precisa compreender o que é uma variável. Este é um conceito presente em quase todas as linguagens de programação, é crucial que você entenda o que é uma variável antes de seguir em frente. O conceito pode ser definido da seguinte maneira:

 “Um espaço alocado na memória do computador que guarda um valor”. 

Tentando abstrair um pouco esta definição, você pode pensar a variável como uma caixa dentro de um quarto cheio de caixas. Cada caixa tem uma palavra escrita nela para identificação e dentro dela algo que você resolveu guardar por algum motivo. 

Em python, variáveis são criadas da seguinte maneira:   

```python
numero = 10
```

Neste caso "numero" é o nome da variável, o sinal ”=” representa a ação de atribuição, ou seja, estamos colocando dentro da caixa etiquetada como “numero” o valor 10.  

### Tipos

Nas linguagens de programação, os valores armazenados dentro das variáveis precisam poder ser classificados em um tipo. O tipo de uma variável se refere a classe na qual pode ser identificado o valor que ela guarda, isto é necessário para que seja possível fazer comparações e operações com as variáveis. No exemplo anterior, a variável “numero” é do tipo inteiro por guardar um valor que se enquadra nesta definição.

Os tipos primitivos que existem em python são apresentados na introdução são Inteiro, Float, String e Booleano.

Inteiro: Qualquer número inteiro, em python a palavra reservada para este tipo é “int”

Float: Todos os números que tenham casas decimais, a palavra reservada para este tipo é “float”

String: Conjunto de caracteres alfanuméricos, a palavra reservada para este tipo é “str”, em python para que seja póssivel reconhecer uma string ela deve sempre estar entre aspas. por exemplo:  

```python
frase = "Eu amo estudar programação"
frase_com_erro = eu amo estudar programação
```

Sem o uso de aspas, a linguagem python não conseguirá interpretar que o que você escreveu é uma string.

Booleano: O tipo booleano representa apenas dois valores, True ou False, você entenderá melhor os casos de uso deste tipo na sessão que ensina sobre condicionais. 

Obs: Você perceberá a importância dos tipos nas próximas sessões e entenderá as operações que podem ser realizadas entre com cada um deles. Por enquanto, o mais importante é que você entenda a definição e conheça cada um deles.

Em python o tipo de uma variável é dinâmico, isso significa que o tipo muda de acordo com o valor que está armazenado nela, por exemplo:

```python
minha_variavel = "Eu amo estudar programação"
minha_variavel = 10
```

Na primeira linha “minha variável” estará guardando a string "Eu amo estudar programação", dessa forma o seu tipo é “str”, após a segunda linha o tipo dela será alterado para “int” pois agora ela guarda um valor do tipo inteiro. É importante que você perceba que ao fazer uma atribuição à uma variável o valor dentro dela é atualizada e o que estava gravado anteriormente será perdido, ou seja, variáveis do tipo primitivo podem armazenar um único valor por vez.

Exercício:

Informe qual é o tipo de cada uma das seguintes variáveis:

 

```python
var_1 = False
var_2 = 0.13
var_3 = 13
var_4 = "Python é legal"
```

### Expressões aritméticas

No universo da programação existem os operadores aritiméticos, relacionais e os lógicos, neste momento serão apresentados os operadores que possibilitam as expressões aritiméticas.

Enquanto desenvolvemos um programa é muito comum precisarmos utilizar funções aritiméticas como as que vemos na escola(soma, subtração, multiplicação, divisão e algumas outras), para isto ser possível, as linguagens de programação disponibilizam operadores que realizam estas funções. Em python estes operadores são:

+ : Para a soma.

```python
total = 5 + 8 #A variável guardará o resultado da operação aritimética que é 13.
```

- : Para a subtração. 

```python
total = 13 - 5 #A variável guardará o resultado da operação aritimética que é 8.
```

* : Para multiplicação.

```python
total = 13 * 5 #A variável guardará o resultado da operação aritimética que é 65.
```

/ : Para divisão.

```python
total = 12 / 6 #A variável guardará o resultado da operação aritimética que é 2.
```

** : Para potencia.

```python
total = 13 ** 2 #A variável guardará o resultado da operação aritimética que é 169.
```

// : Para divisão inteira.

É comum que não ter familiaridade com esta operação, o seu papel é semelhante ao de uma divisão, porém o resultado sempre será sempre um número inteiro. 

```python
total = 13 // 2 #A variável guardará o resultado da operação aritimética que é 6.
total = 15 // 2 #A variável guardará o resultado da operação aritimética que é 7.
total = 21 // 4 #A variável guardará o resultado da operação aritimética que é 5.
```

% : Para módulo.

É comum que não ter familiaridade com esta operação, o seu papel é semelhante ao de uma divisão, porém o resultado sempre será sempre o resto da divisão. 

```python

total = 21 % 2 #A variável guardará o resultado da operação aritimética que é 1.
total = 21 % 3 #A variável guardará o resultado da operação aritimética que é 0.
total = 20 % 3 #A variável guardará o resultado da operação aritimética que é 2.
```

() : Para definir a precedência das operações.

```python
total = 21 % (2 * 4) + 3 #A variável guardará o resultado da operação aritimética que é 8.
total = 21 % 2 * (4 + 3) #A variável guardará o resultado da operação aritimética que é 7.
```

As expressões aritiméticas podem ser usadas em conjunto para conseguir representar qualquer grau de complexidade que se deseje, por exemplo, não existe um operador específico para rediciação, porém, juntando o operador de potência com o de divisão é possível conseguir o efeito de uma raiz da seguinte forma:

```python
total = 169 ** (1/2) #A variável guardará o resultado da operação aritimética que é 7.
```

### Entrada e saída

Dentro do mundo da programação nós tratamos todos os problemas fazendo o seguinte passo a passo:

1. Recebemos entradas de informações abstraídas do mundo real;
2. Processamos essas informações para conseguir resolver a problemática para a qual aquele programa está sendo desenvolvido;
3. Retornamos essa informações agora processadas e com as “respostas” para os problemas encontrados para o usuário;

Toda e qualquer situação precisa passar por todas essas etapas para poder resolver problemas reais.

Em python recebemos dados através do comando:

```python
input("Escreva um número")
```

Esse comando serve para que o programa escrito espere uma entrada de informação do usuário.

O processamento é feito durante a execução do programa, por exemplo, somar dois números que recebemos do usuário, calcular a média após receber as notas de um aluno, ordenar uma lista de compras pelo preço após um usuário nos entregar todas as coisas que ele deseja comprar;

Já a saída pode ser feita de várias formas, a mais simples é o comando print(). Esse comando serve como uma forma de exibir algo para o usuário como por exemplo o valor da soma dos números que ele escreveu, a média, a lista ordenada. Esse comando mostra no seu terminal a informação que você passar para ele.

Veja um exemplo:

```python
print("printei")
```

## Exercícios

1. Crie um programa que vai armazenar três valores, o valor de x = 3, y = 4 e soma = x + y e printe o valor de soma na tela. Declare duas variáveis, a e b, com os valores 10 e 20, respectivamente. Depois, crie uma variável total que some a e b. Por fim, imprima o valor de total.
2.  Escreva um programa que leia o ano de nascimento de uma pessoa e calcula e imprime no console a idade dela.
3. Crie duas variáveis, largura e altura, com os valores 5 e 7, respectivamente. Calcule a área de um retângulo usando essas variáveis e armazene em uma variável chamada area. Imprima o valor de area.
4. Sabe-se que o m² de construção custa R$820. Escreva um programa que leia as medidas de um terreno retangular e calcula e imprime quanto custa para construir uma casa que ocupe esse terreno. 
5. Crie uma variável base com o valor 3 e outra variável expoente com o valor 4. Calcule base elevado a expoente e armazene o resultado em uma variável chamada potencia. Imprima o valor de potencia.
6. Declare uma variável numerador com o valor 17. Divida numerador por 3 usando divisão inteira e armazene o resultado em uma variável chamada resultado. Imprima o valor de resultado.
7. Declare uma variável numero com o valor 29. Calcule o resto da divisão de numero por 5 e armazene o resultado em uma variável chamada resto. Imprima o valor de resto.
8. Declare uma variável resultado e armazene o valor da expressão 10 + 2 * 3 - 1. Imprima o valor de resultado.
9. Declare uma variável resultado e armazene o valor da expressão (10 + 2) * (3 - 1). Imprima o valor de resultado.
10. Peça ao usuário para digitar dois números e armazene-os em variáveis chamadas num1 e num2. Some os dois números e armazene o resultado em uma variável chamada soma. Imprima o valor de soma.
11. Uma loja está oferecendo um grande desconto: *para as clientes que levarem 4 produtos, será dado um desconto de 20% no valor total da compra*. Crie um programa que leia o preço dos 4 produtos e calcule e imprima no console: o valor do total da compra sem desconto, quanto foi o desconto e quanto deverá ser pago.
12. Escreva um programa que leia o salário total de uma pessoa e quantas horas ela trabalha por dia. Em seguida, calcule e imprima quanto essa pessoa recebe por hora.
13. Um estudo mostrou que o lucro de uma viagem estadual é 55% vindo de pessoas que pagam a passagem inteira e 45% de estudantes que pagam meia. Uma passagem de ônibus custa 30 reais. Sabendo disso, crie um programa que leia quanto a empresa de ônibus acumulou no caixa após um dia de trabalho e calcule e exiba a estimativa de quantos passageiros de cada tipo andaram de ônibus naquele dia.
14. Crie um programa que receba uma temperatura em Celsius, a converta e exiba usando as escalas Kelvin e Fahrenheit [entenda mais sobre essa conversão aqui](http://www.infoescola.com/fisica/conversao-de-escalas-termometricas/). 
    K=C+273
    F=1,8C+32