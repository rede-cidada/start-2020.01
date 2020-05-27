# DOM

## O que é o DOM?

No início, o JavaScript e o DOM estavam fortemente interligados, mas, eventualmente, evoluíram para entidades separadas. O conteúdo da página é armazenado no DOM e pode ser acessado e manipulado via JavaScript.

Embora o DOM seja frequentemente acessado usando JavaScript, não é uma parte da linguagem JavaScript. Ele também pode ser acessado por outras linguagens.

Quando uma página da web é totalmente carregada, o navegador cria um DOM da página. O DOM é a representação de dados dos objetos que compõem a estrutura e o conteúdo de um documento na web.

O DOM trata um documento como uma árvore de objetos em que cada nó representa uma parte do documento. Para permitir que você entenda a árvore de objetos DOM.

Vamos converter os elementos HTML do código abaixo em uma árvore de objetos DOM.

```markup
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>O DOM</title>
  </head>
  <body>
    <h1>Programa Start</h1>
    <p>Somos a melhor turma de Frontend em linha reta do planeta!</p>
  </body>
</html>
```

![Representa&#xE7;&#xE3;o da &#xE1;rvore de objetos do DOM.](.gitbook/assets/image.png)

E como você pode ver, o primeiro elemento `<html>` no código é o nó mãe da árvore, enquanto os elementos `<head>` e `<body>` são nós filhos do nó mãe `<html>`. O `<title>` e os `<meta>` são filhos do elemento `<head>`, enquanto os elementos `<h1>` e o `<p>` são nós filhos do elemento `<body>`. Se você já ouviu falar sobre a árvore genealógica em biologia, pense na árvore de objetos DOM como uma réplica semelhante da árvore genealógica

## Acessando o DOM <a id="How_Do_I_Access_the_DOM.3F"></a>

> Você não precisa fazer nada de especial para começar a usar o DOM, todo navegador usa um modelo de objeto de documento para tornar as páginas da web acessíveis via JavaScript.

### Métodos de acesso DOM

O DOM possui muitos métodos, são eles que fazem a ligação entre os nodes \(elementos\) e os eventos. Vamos estudar os métodos mais usados lembrando que existem muitos outros e você pode ver todos [nesse link](https://developer.mozilla.org/en-US/docs/Web/API/Document).

### Selecionando elementos pela identificação

Qualquer elemento HTML pode ter um atributo id. O valor desse atributo deve ser único dentro do documento - dois elementos no mesmo documento não podem ter a mesma identificação. Você pode selecionar um elemento com base nessa identificação exclusiva com o método getElementById\(\) do objeto document.

```markup
<h1 id="title">Programa Start</h1>
```

```javascript
// index.js
const elementTitle = document.getElementById("title");

// Recuperando o valor:
console.log(elementTitle.innerText); // Programa Start

// Alterando o valor:
elementTitle.innerText = "Programa Start 2020";

// Recuperando o novo valor:
console.log(elementTitle.innerTextß); // Programa Start 2020
```

### Selecionando elementos pelo nome

A atributo HTML name se destinava originalmente a atribuir nomes a elementos de formulário e o valor desse atributo é usado quando dados de formulário são enviados para um servidor. Assim como o atributo id, name atribui um nome a um elemento. Ao contrário de id, contudo, o valor de um atributo name não precisa ser único: vários elementos podem ter o mesmo nome e isso é comum no caso de botões de seleção e caixa de seleção em formulários web. Além disso ao contrário de id, o atributo name é válido somento em alguns elementos HTML, incluindo formulários, elementos de formulário, tag iframe e tag img.

```markup
<!-- HTML -->
<input type="radio" name="techs" value="react"/>
<input type="radio" name="techs" value="vue"/>
<input type="radio" name="techs" value="angular"/>
```

```javascript
//
// JavaScript
//
const elementos = document.getElementsByName("techs");
console.log(elementos);
// NodeList(3) [input, input, input]

// Podemos acessar cada elemento, individualmente, através de seu índice.
console.log(elementos[0].value); // react
console.log(elementos[1].value); // vue
console.log(elementos[2].value); // angular

// Podemos alterar esses valores também:
elementos[2].value = "svelt"
console.log(elementos[2].value); // svelt
```

### Selecionando elementos pela tag

`getElementsByTagName` permite você percorrer o DOM procurando por todos os elementos em sua página com um nome de tag especificado. Aqui está a sintaxe:

```markup
<ul>
  <li>React</li>
  <li>Vue</li>
  <li>Svelt</li>
  <li>Angular</li>
</ul>
```

```javascript
const items = document.getElementsByTagName('li');
// HTMLCollection(4) [li, li, li, li]
```

### Métodos `node`

![M&#xE9;todos pra navegar pela &#xE1;rvore do DOM](.gitbook/assets/image%20%282%29.png)

Tenho certeza de que poderia escrever alguns parágrafos sobre os diferentes métodos de acessar "nós" no DOM, mas acho que uma visão geral básica das possibilidades será suficiente para nossos propósitos aqui. Um "nó" é essencialmente qualquer elemento da sua página na estrutura do DOM, incluindo espaço em branco e texto entre tags HTML.

Os diferentes métodos de nó disponíveis através da manipulação do DOM são os seguintes:

```javascript
node.childNodes
node.firstChild
node.lastChild
node.parentNode
node.nextSibling
node.previousSibling
```

Em cada exemplo acima, o `node` seria o objeto que você está fazendo referência. Vamos ilustrar a diversidade desses métodos usando um exemplo simples:

```markup
<ul id="list">
  <li class="primeiro-item">React</li>
  <li>Vue</li>
  <li>Svelt</li>
  <li>Angular</li>
</ul>
```

> Podemos acessar o primeiro item lista acima usando qualquer uma das três opções a seguir:

```javascript
const minhaListaDeItens = document.getElementById("list"); 
const meuPrimeiroItem = minhaListaDeItens.childNodes[1].className; // primeiro-item
```

```javascript
const minhaListaDeItens = document.getElementById("list"); 
const meuPrimeiroItem = minhaListaDeItens.firstElementChild.className; // primeiro-item
```

```javascript
const minhaListaDeItens = document.getElementById("list"); 
const meuPrimeiroItem = minhaListaDeItens.firstChild.nextSibling.className; // primeiro-item
```

