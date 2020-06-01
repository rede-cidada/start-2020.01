---
description: >-
  Olá, seja bem vindo ao mundo da Lógica de Programação. Aqui vamos aprender
  algumas regras e conceitos que são fundamentais para o mundo da computação,
  como algoritmo, tipos e estruturas de dados.
---

# Lógica de Programação

### **Índice**

1. O que é lógica de programação?
2. Regras e conceitos
   1. Algoritmos
   2. Pseudocódigo
   3. Fluxograma
   4. Variáveis e Constantes
   5. Tipos de dados
   6. Operadores e expressões 
      1. Aritméticos
      2. Atribuição
      3. Comparação
      4. Lógico
   7. Estruturas de decisão e repetição
      1. IF/ELSE
      2. SWITCH
      3. WHILE
      4. DO-WHILE
      5. FOR
   8. Funções
   9. Sintaxe e semântica
3. Referências Bibliográficas

### **O que é lógica de programação?**

É um conjunto de regras e conceitos que nos ajudam a criar um código escrito.

Na área de computação é muito importante saber lógica de programação e entender como utilizar na resolução de problemas através da programação. mais adiante vamos aprender as regras e conceitos, e como utilizá-los.

### **Regras e Conceitos**

### **Algoritmos**‌

Temos vários conceitos para algoritmos, são elas:

> “Um algoritmo é uma sequência de passos que visa atingir um objetivo especíﬁco” \(ASCENCIO, 2002 apud FORBELLONE, 1999\)

> “É a descrição e uma sequência de passos que deve ser seguida para a realização de uma tarefa” \(ASCENCIO, 2002 apud ASCENCIO, 1999\)

Através dos conceitos acima, podemos definir algoritmo como sendo uma sequência de ações a serem feitas com a finalidade de executar uma tarefa.

Vamos ver o exemplo de um algoritmo abaixo:

```text

1 - Pegar o primeiro número
2 - Pegar o segundo número
3 - Somar o primeiro número com o segundo número 
4 - Mostrar o resultado  da soma

```

### **Pseudocódigo**

É a maneira como o algoritmo é escrito para o programador. A seqüência de ações a serem feitas devem ser descritas de forma simples e objetiva. Para isso, é necessário ter em mente as seguintes regras:

* Usar apenas um verbo por frase;
* Usar frases curtas e simples;
* Ser objetivo.

Exemplo de algoritmo escrito em pseudocódigo de como **Fritar ovos**:

```text
1 - Primeiro deve-se pegar os ovos
2 - Depois pegar a manteiga
3 - Em seguida pegar uma frigideira
4 - Deve-se acender o fogo
5 - Colocar a manteiga na frigideira
6 - Quebrar os ovos na frigideira
7 - Colocar a frigideira no fogo
8 - Por fim fritar ovos
```

Exercício:

1. Fazer um pseudocódigo de um algoritmo com 15 linhas no máximo.

### **Fluxograma**

É uma forma de representar o algoritmo graficamente. Através de figuras geométricas, podemos representar passo a passo as instruções do algoritmo.

![Fonte:N&#xFA;cleo de Tecnologia Digital Aplicada &#xE0; Educa&#xE7;&#xE3;o \[4\]](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M83Im6iZekEOJbxxNao%2F-M83IwBrNAcOCuGCt5ev%2FScreen%20Shot%202020-05-23%20at%2022.32.07.png?alt=media&token=2e6bb91b-58fd-4032-931d-24762d55e9a3)

Exemplo de fluxograma do algoritmo para **Trocar lampada**.

![Fonte: https://programecmg.wordpress.com \[5\]](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M83JGFyLdFeqscvo74D%2F-M83KIvXRSq3nf3Aju1Z%2Fimages01.png?alt=media&token=085123b9-d421-4890-afd8-8997913b880a)

**Exercício:**

1. Desenhar o fluxograma do algoritmo criado na sessão anterior.

### **Variáveis e Constantes**

**Variável** é um espaço na memória do computador onde um dado será armazenado, esse dado pode ser alterado. 

**Constante** é uma variável onde o dado armazenado não pode ser alterado. para declarar uma constante usamos a palavra especial **const**. 

Exemplo: 

const nomeDaVariavel = \(valor da variável\) 

As variáveis podem ser: Globais e Locais.   
Globais: São as variáveis que podem ser acessadas de qualquer lugar.   
Locais: São as variáveis que podem ser acessadas apenas no bloco de código que foram declaradas. 

**Importante**: O **nome** da variável é seu **IDENTIFICADOR**, ou seja, o nome da variável deve ser único.

**Regras para nomes de variáveis**

1. Podem ter letras do alfabeto\(minúsculas ou maiúsculas\), dígitos \(0 … 9\) e o caractere _underline_ \(\_\);
2. O primeiro caractere não pode ser um dígito, ex: 9nome;
3. Maiúsculas e minúsculas são diferentes \(case-sensitive\), ex: nomeCliente &lt;&gt; nomecliente;
4. Não pode ser uma palavra reservada, ex: _for_, _if_, _int_;
5. Não é aconselhável o uso de caracteres acentuados, ex: nomeUsuario;
6. O nome deve ser identiﬁcador do que armazena, ex: codigoCliente no lugar de x;
7. Não deve ser todo escrito em maiúsculas, ex: NOMECLIENTE;
8. Usar _undeline_ ou a diferença entre maiúsculas e minúsculas \(camelCase\) caso o nome use mais de uma palavra, ex : nome\_cliente ou nomeCliente;
9. Não usar _undeline_ para iniciar o nome de variáveis, ex: \_nomecliente;

Exemplos válidos de nomes de variáveis:

* nome\_Cliente\_10
* nomeCliente
* telefoneEmpresa
* telefone\_empresa
* endereco1

### **Tipos de dados**

O **tipo de um dado** define o tipo do valor que a variável vai conter. Por exemplo: Se existir uma variável que aceita apenas dado numéricos quer dizer que o tipo do dado dessa variável é **numérico.**

Sintaxe para declaração de variável com tipo de dados

```text
tipo var1 [, var2, ..., varn ]
```

**Tipos primitiv**

Os tipos primitivos representam os tipos mais simples de dados. na tabela abaixo pode-se ver quais são os tipos primitivos.

Os numéricos podem ser Inteiros \(positivos ou negativos\) e Reais \(decimais podendo ser positivos ou negativos\).

Exemplos: 

**1** -&gt; é um número inteiro positivo   
**-1** -&gt; é um número inteiro negativo   
**0** -&gt; é um número inteiro positivo   
**1.0** -&gt; é um número real positivo com uma casa decimal   
**1.1** -&gt; é um número real positivo com uma casa decimal   
**-1.123** -&gt; é um número real negativo com três casas decimais 

Os caracteres podem ser letras, números, símbolos ou espaço. Usa-se as aspas \("\) no início e no término do valor de caracteres. Dizemos que uma string é um conjunto de caracteres, e um char é um caracter.

Exemplos: 

**"ana maria"** -&gt; é uma string pois é uma sequencia de caracteres   
**"a"** -&gt; é um char pois é apenas um caracter   
**" "** -&gt; é o caracter vazio \(espaço em branco\)   
**"1"** -&gt; é um caracter pois está entre aspas mesmo sendo um numeral.   
**";&gt;="** -&gt; é uma string pois é uma sequencia de caracteres mesmo sendo eles símbolos 

Os booleanos são valores lógicos, que possuem apenas dois valores verdadeiro e falso.

Exemplos: 

true - verdadeiro false - falso

Exemplo de declaração de variável com tipo de dados

```text
boolean  moraComSuaMae
(tipo)  (nome da variável)
```

Exercício:

1. Escreva a declaração de uma variável do tipo booleano de nome x.
2. Escreva a declaração de uma variável do tipo caractere de nome carro.
3. Escreva a declaração de uma variável do tipo caractere de nome \(escolha um nome válido\) que tenha o valor carro21!.
4. Escreva a declaração de uma variável do tipo booleano de nome \(escolha um nome válido\) que tenha o valor 35.
5. Escreva a declaração de uma variável do tipo numérico de nome \(escolha um nome válido\) que recebe o valor papagaio.

**Operadores e expressões**

São símbolos especiais que tem um signiﬁcado próprio para as linguagens de programação e estão associados a determinadas operações. Temos quatro tipos: aritméticos, atribuição, comparação e lógico.

**Operadores aritméticos**

* Soma `+`
* Subtração `-`
* Multiplicação `*`
* Divisão `/`
* Exponenciação `**`
* Módulo \(resto da divisão\) `%`
* Incremento `++`
* Decremento `--`

Exemplos:

```text
b + c;
b - c;
b / d;
b * d;
```

**Operadores de atribuição**

* Igual `=` ---&gt; `x = y`
* Adiciona valor `+=` ---&gt; `x = x + y`
* Subtrai valor `-=` ---&gt; `x = x - y`
* Multiplica valor `*=` ---&gt; `x = x * y`
* Divide valor `/=` ---&gt; `x = x / y`

Exemplos:

```text
var a = b + c;
var a = b - c;
var a = b / d;
var a = b * d;
```

**Operadores de comparação**

* Igual a `==` `===` \(mesmo valor e mesmo tipo\)
* Não é igual a `!=` `!==` \(mesmo valor e mesmo tipo\)
* Maior que `>`
* Menor que `<`
* Maior ou igual que `>=`
* Menor ou igual que `<=`
* Operador ternário `?`

Exemplos:

```text
var a = 2 > 1;
var a = 2 == "2";
var a = 1 !== "1";
var a = 3 >= 4 ? true : false;
```

**Operadores lógicos**

* E `&&` --&gt; Retorna true se as duas expressões forem verdadeiras
* OU `||` --&gt; Retorna true se pelo menos uma das expressões for verdadeira
* Negação `!` --&gt; Retorna true se o valor for falso e retorna false se o valor for verdadeiro.

Exemplos

```text
b == c && c > d 
a >= b || d < a
!c || !b
‌
```

### **Estrutura de decisão**

São estruturas que utilizamos para tomar a decisão de qual ação fazer. Temos condições e vemos qual é verdadeira ou falsa.

**IF e ELSE**   
Quando temos mais de um caminho a seguir, usamos o **if \(se\)** para decidir qual condição temos que cumprir para alcançar nosso objetivo, e o **else \(se não\)** para ser nosso caminho alternativo.

Estrutura do If/Else

```text
if(condição)
  comandos;
else
  comandos;   
```

Exemplo: Estamos cozinhando e provamos uma comida, **se** estiver sem sabor então colocamos sal, e **se não** estiver sem sabor, podemos colocar pimenta ou não fazer nada.

```text
if comida sem sabor
  coloque sal
```

```text
if comida sem sabor
  coloque sal
else
  coloque pimenta  
```

**SWITCH**   
O switch é uma estrutura de decisão que diante de uma condição ele seleciona o que será feito. Este comando é muito utilizado para a construção de menus de opções ao usuário.

Estrutura do Switch

```text
switch (expressao) {
    case valor1:
        comandos;
        break;
    case valor2:
        comandos;
        break;
   ...
    default:
        comandos;
}

```

Exemplos:

```text
switch (dias da semana) {
    case segunda-feira:
        estudar;
        break;
    case terça-feira:
        jogar video-game;
        break;
    case quarta-feira:
        ir ao cinema;
        break;
     ...
    default:
        dormir;
}

```

### **Estrutura de repetição**‌

São estruturas que utilizamos para repetir a execução algumas ações enquanto uma condição permanecer verdadeira.

**WHILE**   
O comportamento do While é muito diferente do comportamento do comando IF/ELSE. Em uma condição, é analisada se a resposta for true ou false, então uma ação é realizada, ou não, uma única vez.

Estrutura do While

```text
while (expressão) {
 comandos;
 ...
} 
```

Exemplos:

```text
while (dia da semana é segunda-feira?) {
acordar cedo;
estudar;
} 

```

**DO-WHILE**   
Os comandos do DO-WHILE só serão executados se a condição for verdadeira.

Estrutura do While

```text
do {
  comandos;
 ...
} 
while (expressão) 

```

Exemplos:

```text
do {
  acordar_cedo();
  estudar();
} 
while (dia da semana é segunda-feira)

```

‌**FOR**

 O comando FOR pode ser utilizado quando precisar repetir algumas ações um determinado número de vezes. É importante tomar cuidado, pois a repetição deve ter um fim, caso contrário, o seu programa ficará sendo executado infinitamente \(chamamos de loop infinito\).

Estrutura do For

```text
for(expressão inicial; condição; expressão final){
    comandos;
}
```

1. **expressão inicial** - cria a variável de controle e a mesma é iniciada. 
2. **expressão2** - condição de continuação do laço. 
3. **expressão3** - modiﬁca o valor da variável de controle.

Exemplos:

```text
for (var dias = 1, i <= 5; i++){
    estudar();
}
```

Exercícios

1. Faça um algoritmo para ler um número inteiro e informar se este é maior que 10.
2. Faça um algoritmo para ler dois números inteiros e informar se estes números são iguais ou diferentes.
3. Faça um algoritmo para ler um número inteiro e informar se o número é par ou ímpar. 
4. Faça um algoritmo para ler dois números inteiros A e B e informar se A é divisível por B.

**Funções**

Funções são blocos de código que executam determinada atividade. As funções são utilizadas quando são chamadas \(opa como assim chamadas?\) Quando dizemos que as funções são chamadas significa que elas são referenciadas.

Estrutura de função

```text
function nomeDaFuncao(parametro1, parametro2) {
    return parametro1 * parametro2;
}
```

1. _function_ é a palavra-chave usada para criar funções 
2. **nomeDaFuncao** é o nome da função
3. Entre parênteses após o nome da função estão os parâmetros de entrada da função \(são opcionais\)
4. _return_ é a palavra-chave usada para especiﬁcar o retorno da função 
5. O escopo \(recursos\) de uma função é delimitado por chaves \( **{...}** \)

Exemplos:

```
function somarDoisNumeros(valorA, valorB) {
 return valorA + valorB;  
}
```

```text
function somarDoisNumeros(valorA, valorB) {
   let resultado = valorA + valorB;  
   return resultado;
}
```

**Sintaxe e Semântica**

> Na Engenharia de Software quando falamos de sintaxe geralmente nos referimos à forma de escrever código fonte \(palavras reservadas, comandos, recursos diversos\).   
> Quando falamos de semântica, nos referimos ao significado dos modelos, ao nível de entendimento \(clareza, objetividade, detalhamento, coesão etc.\) de alguma coisa.   
> Fonte: [https://www.ateomomento.com.br/](https://www.ateomomento.com.br/) \[11\]

Lendo o texto acima, entendemos que sintaxe e semântica tem a ver com boa escrita e bom conteúdo para um bom entendimento. É importante lembrar sempre que quando escrever um código devemos buscar as melhores práticas para escrever um código de fácil compreenção.

Podemos utilizar técnicas simples para facilitar a escrita e leitura de um código, o objetivo é deixar o código mais fácil de entender o que de fato deve-se fazer com ele. Podemos fazer algumas ações como: 

1 - Utilizar nomes em variáveis e funções que sejam fácil entendimento do que são e do que fazem.   
2 - Evitar nomes repetidos de variáveis.   
3 - Evitar código duplicado.   
4 - É melhor fazer várias funções pequenas ao invés de fazer uma função muito grande.   
Essas são apenas algumas ações que podemos fazer para ter boas sintaxe e semântica em nossos algoritmos e códigos.

**Referências Bibliográficas:**

\[1\] [https://www.impacta.com.br/blog/2017/03/24/entenda-o-que-e-logica-de-programacao/](https://www.impacta.com.br/blog/2017/03/24/entenda-o-que-e-logica-de-programacao/)   
\[2\] [https://www.infoescola.com/informatica/logica-de-programacao/](https://www.infoescola.com/informatica/logica-de-programacao/)   
\[3\] [https://www.devmedia.com.br/logica-de-programacao-introducao-a-algoritmos-e-pseudocodigo/37918](https://www.devmedia.com.br/logica-de-programacao-introducao-a-algoritmos-e-pseudocodigo/37918)   
\[4\] [http://www.nuted.ufrgs.br/oa/animak/nocoes.php](http://www.nuted.ufrgs.br/oa/animak/nocoes.php)   
\[5\] [https://programecmg.wordpress.com/2013/03/28/algoritmos/](https://programecmg.wordpress.com/2013/03/28/algoritmos/)   
\[6\] [https://www.embarcados.com.br/variaveis-e-constantes/](https://www.embarcados.com.br/variaveis-e-constantes/)   
\[7\] [https://www.dimap.ufrn.br/~richard/pubs/dim0320/readings/aula03.pdf](https://www.dimap.ufrn.br/~richard/pubs/dim0320/readings/aula03.pdf)   
\[8\] ASCENCIO, A. F. G. e CAMPOS, E. A. V. de. **Fundamentos da Programação de Computadores**. 1ed. São Paulo: Pearson Prentice Hall, 2002.   
\[9\] [https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Lacos_e_iteracoes)/   
\[10\] [https://www.ic.unicamp.br/~wainer/cursos/2s2011/Cap06-RepeticaoControle-texto.pdf](https://www.ic.unicamp.br/~wainer/cursos/2s2011/Cap06-RepeticaoControle-texto.pdf)   
\[11\] [https://www.ateomomento.com.br/sintaxe-e-semantica-forma-e-conteudo-na-producao-de-software/](https://www.ateomomento.com.br/sintaxe-e-semantica-forma-e-conteudo-na-producao-de-software/)   
\[12\] [https://medium.com/joaorobertopb/1-clean-code-o-que-é-porque-usar-1e4f9f4454c6](https://medium.com/joaorobertopb/1-clean-code-o-que-%C3%A9-porque-usar-1e4f9f4454c6)

