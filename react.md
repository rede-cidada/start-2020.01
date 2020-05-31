# React

## O que é React e pra que serve?

> Apesar de muitos confundirem, o React não é um framework e sim uma biblioteca.

## Tá, mas qual a diferença entre framework e biblioteca?

Framework é um conjunto de funções e módulos que resolvem vários problemas diferentes, por exemplo: o Angular resolve problemas de rotas e views ao mesmo tempo e mais uma porrada de outras necessidades... Diferentemente do React que foca em resolver o "problema" de renderização da View. Ué mas e se eu quiser usar rotas no React? — Simples, você terá que importar uma biblioteca que resolve o problema de rota.

> FONTE: Palavras da Deva Laryssa Magalhães [nesse artigo aqui!](https://medium.com/@larymagal/react-para-iniciantes-f09360a24786)

React é uma biblioteca criada pelo Facebook e é usado basicamente para construir páginas web, tipo essa aqui que você está lendo esse conteúdo. O legal é que ele constroi páginas de forma declarativa, isso significa que basicamente declaramos como que a nossa página vai reagir a um estado ou a como um dado se comporta.

## O que é o Virtual DOM?

Antes de falar sobre virtual DOM vamos relembrar sobre o DOM. Vimos na sessão do DOM como alterar a nossa página adicionando, alterando ou removendo os elementos dela, porém esse processo de realizar essas mudanças diretamente no DOM causa lentidão para renderizar novamente o elemento por não ser um processo muito performático.

Virtual DOM é uma técnica que o React usa pra atualizar a tela onde é construido os dados a ser apresentado na tela, ele nada mais é que um objeto virtual que representa o DOM real. Você pode ler [esse artigo](https://medium.com/roliveiradev/por-que-getelementbyid-deve-ser-evitado-6b0d35d055fe) que explica detalhadamente todo esse processo de DOM e Virtual Dom.

## Mão na massa

Para entendermos os próximos conceitos vamos criar juntas essa pequena aplicação usando React.

![Imagem da aplica&#xE7;&#xE3;o que vamos criar juntas nessa se&#xE7;&#xE3;o.](.gitbook/assets/image%20%285%29.png)

### O que é componente?

As aplicações em React são baseadas em componentes que são pequenos blocos de códigos que podem ser reutilizados. Esses blocos são funções que podem receber dados de entrada como parâmetros, retornam um elemento React através do `JSX` e no final esses são transformados no DOM Virtual e mostrados na tela através do `DOM`.

Agora vamos tentar entender tudo isso através da nossa aplicação que conterá os seguintes componentes:

1. Componente `<Message />` que retorna um `<h1>` com uma mensagem.
2. Componente `<Figure />` que retorna um `<img>` com uma imagem.
3. Componente `<Button />` que retorna um `<button>` com um texto.
4. Existe uma lista de palavras que são reservadas do javascript que não conseguimos utilizá-las no retorno do nosso componente React, por exemplo `class` que usamos para por estilo no nosso componente é substituída por `className`.
5. Componente `<App />` que retorna uma `<div>` com todos os componentes que criamos e na ordem que eles devem ser apresentados na tela.
6. Por fim teremos o `index.js` que terá o método para de fato renderizar nosso componente `<App/>` no `DOM` e fazer com que o usuário possa visualizar nossa aplicação.

Abaixo está uma representação da nossa aplicação dividida por componentes, se olharmos com atenção podemos fazer uma analogia dos componentes que são pequenos blocos de códigos à pequenos blocos de lego que quando unimos os componentes montamos nossa aplicação, da mesma forma como conseguimos montar qualquer coisa com os pequenos blocos de lego.

![](.gitbook/assets/image%20%284%29.png)

### 1. Criando o componente`<Message />`

Como já falamos, componentes são funções que retornam um elemento `React`, então bora tentar criar uma função para representar nosso componente `Message`.

Antes de iniciar a desenvolver nosso componente vamos ter alguns pontos de atenção, não se preocupe se não entender todos os conceitos agora, iremos entrar em detalhes sobre todos mais tarde:

1. Todo componente React deve iniciar com a letra maiúscula.
2. No retorno do nosso componente, códigos javascript só funcionam se forem envolvidos por chaves`{}`.
3. Todo componente React precisa importar a função `React`.
4. Todo componente deve retornar um único elemento, então fazendo uma analogia com o que aprendemos no `HTML`, o retorno de um componente React não pode conter irmãos nesse caso devemos envolvê-lo em um outro elemento, ou seja, no retorno de um componente React todos elementos tem sempre um único `pai`, veja o exemplo abaixo:

   ```markup
     // Assim não funciona
     <div>...</div>
     <div>...</div>

     // Assim funciona
     <div>
       <div>...</div>
       <div>...</div>
     </div>
   ```

Aqui está nosso componente `Message`, que nada mais é que uma função que retorna uma mensagem:

```javascript
// Message.js
import React from 'react' // importando o react

// criando nosso componente
export const Message = () => <h1>Hello World React</h1>
```

### 2. Usando o componente`<Message />` e criando o componente `<App />`

Beleza, já temos nosso componente `Message`, agora em todas as páginas que a gente precisar mostrar essa mensagem é só importar nosso componente e usá-lo, veja o exemplo abaixo onde estamos usando ele no componente `App`:

```javascript
// App.js
import React from 'react' // importando o react
import { Message } from './Message' // importando nosso componente

// criando o cmponente <App/>
export const App = () => (
  <div className="App">
    {/* usando nosso componete */}
    <Message />
  </div>
)
```

### 3. O que é `JSX`?

Vamos dá uma pausa na nossa aplicação para entendermos o que é `JSX`.

Para construir o virtual DOM é preciso criar uma sequência de instruções pra manipular a árvore do `DOM`. Construir com javascript a estrutura do HTML é um processo bem complexo, passamos por isso quando estudamos sobre a API do DOM. Por isso o time do React desenvolveu uma forma de escrever algo parecido com `HTML` porém que fosse traduzido facilmente para javascript, e isso é o `JSX`, ele tem uma estrutura muito parecida com `HTML` mas não é `HTML`, ele é convertido pra javascript que gera o virtual DOM.

Você não consegue utilizar algumas palavras que são reservadas do javascript nos componentes React, por exemplo o atributo `class` no JSX a gente usa a palavra `className` porque no javascript `class` é reservada pra criação de classes. Veja [nesse link](https://pt-br.reactjs.org/docs/dom-elements.html) todas as palavras que são reservadas no javascript e qual as palavras que usamos para representá-las no React.

Usamos o `JSX` no método `return` do nosso componente e sempre que for preciso usar código javascript dentro do `JSX`, o javascript precisa está envolvido por chaves`{}`. É comum usamos javascript misturado com `JSX` pra retornarmos por exemplo valores dinâmicos usando variáveis, não se preocupe se até agora as coisas não estão fazendo muito sentido, veremos tudo isso na criação da nossa aplicação.

Vejamos no exemplo abaixo um componente com e sem o JSX:

```javascript
import React from "react"; // importando o react

// exemplo de um componente de função usando JSX
const Hello = (props) => {
  return <h1 className="title">Hello {props.name}!</h1>;
};

// o mesmo componente acima sem o uso do JSX
const Hello = (props) => {
  return React.createElement(
    "h1", // o elemento que vai virar HTML
    {
      className: "title" // os atributos são passados nesse objeto
    },
    "Hello ", // aqui vai o conteúdo de texto que ficará dentro do HTML
    props.name, // aqui como é separado o javascript
    "!" // aqui o restante do conteúdo de texto
  );
};
```

Aqui vai algumas respostas dos itens que pontuamos na sessão: Criando o componente`<Message />`

1. Todo componente React deve iniciar com a letra maiúscula.

   1.1 Esse é a forma usada para identificar um elemento React e usar a função `createElement()` para criar um elemento React.

2. Todo componente deve retornar um único elemento.

   2.1 É assim que os parâmetros da função `createElement()` é definido, você pode brincar [aqui nesse link](https://babeljs.io/repl/#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&spec=false&loose=false&code_lz=MYewdgzgLgBAEgUwDZJDAvDAFABwE4g4QCUGAfDADwAWAjDMEgIYQQByTAtgugERQBLKEgS8yiFGgDe-QhAB0YLggC-AQkoB6OmQDcAKEOhIsAII4cGbKXQV9ASEoATAQDcy-mF--PqCJk4IeB7eoTCOEqgwStx8AEr-wFC8MJohYY7a_oHBnuHhlABmICBQQWQAsgEIMADuQtQwqK4IWsWl5Q5aLu5AA&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=react&prettier=false&targets=&version=7.10.2&externalPlugins=) e verificar como ficaria complexo a criação de componentes React sem o uso do `JSX`

3. No retorno do nosso componente, códigos javascript só funcionam se forem envolvidos por chaves`{}`.

   3.1 Essa é a forma que a função `createElement()` usa para diferenciar javascript de simples textos.

### 4. Usando o `ReactDOM.render()`

Até o momento só declaramos alguns componentes porém ainda não conseguimos fazer com que os dados de fato apareça na página. Pra isso, devemos usar o método `ReactDOM.render()` que renderiza um elemento do React no DOM, você pode ler mais sobre ReactDOM [nesse link](https://pt-br.reactjs.org/docs/react-dom.html).

O método `ReactDOM.render()` recebe dois parâmetros, o primeiro é o conteúdo que vai ser que vai ser apresentado na página e o segundo é onde no `DOM` esse conteúdo será inserido para então ser de fato apresentado na página.

Aplicando a teoria acima na nossa aplicação, vamos usar o método `ReactDOM.render()` no arquivo `index.js` que é o primeiro arquivo a ser executado quando uma aplicação é inicializada, veja como utilizamos a cahmada no exemplo abaixo:

```javascript
// index.js

import React from "react"; // importando o react
import ReactDOM from "react-dom"; // importando o ReactDom
import { App } from "./App"; // importando nosso componente <App />

// usando o ReactDOM.render()
ReactDOM.render(
  <App />, // 1º o conteúdo que vamos apresentar na página
  document.getElementById("root"); // 2º onde vamos apresentar esse conteúdo
);
```

Esse elemento que estamos acessando através do `id` está num arquivo chamado `index.html` e esse é o único aruivo `HTML` que temos na nossa aplicação e é nele que é inserido todos os componentes que criamos até agora.

Veja um exemplo da parte no nosso `index.html` onde temos a o `id` que estamos acessando no código acima:

```markup
// index.html

<body>
  <div id="root"></div> <!-- esse é o id que chamamos no ReactDOM.render() -->
</body>
```

### 5. Criando o component

Continuando no desenvolvimento da nossa aplicação vamos criar o componente `<Figure />` que nada mais é que uma função que retorna uma imagem, veja abaixo a estrutura do nosso componente:

```javascript
import React from "react"; // importando o react
import reactImg from "./assets/img/react.png"; // importando a imagem

// criando o cmponente <Figure/>
export const Figure = () => <img className="image" src={reactImg} />;
```

Só um ponto de atenção de como a gente usa imagens no `React`, ela precisa ser importada recebendo um nome, que seria uma variável que vai representar o caminho da imagem, depois usamos essa `variável` no atributo `src` da tag `img`. Note que o valor repassado para o atributo deve ser entre chaves`{}`, já que se trata de um conteúdo `javascript` sendo utilizado dentro do `JSX`.

### 6. O que é `Props` no React?

`Props` é forma de compartilhar informações entre os componentes React, para entender melhor esse conceito vamos criar o componente `<Button />` da nossa aplicação:

```javascript
import React from "react"; // importando o react

// criando o cmponente <Button/>
// repare que agora nosso componente recebe um parâmetro que chamamos de `props`
// poderíamos dá qualquer nome, estamos usando a palavra "props" só por padrão mesmo
// estamos usando a propriedade chamada "tech" que foi um nome também que
// escolhemos pra representar o valor apresentado em cada botão
export const Button = props => <button className="btn">{props.tech}</button>;
```

Agora vamos usar esse componente que criamos lá no nosso `<App />`

```javascript
import React from "react";
import { Message } from "./Message";
import { Figure } from "./Figure";
import { Button } from "./Button"; // importando nosso componente <Button />

export const App = () => (
  <div className="app">
    <Figure />
    <Message name="React" />

    <div className="btn-groups">
      {/* usando nosso componente e criando uma prop chamada "tech" */}
      <Button tech="React" />
      <Button tech="Javascript" />
      <Button tech="JSX" />
    </div>
  </div>
);
```

Se você prestar atenção vai ver que usamos as props da mesma forma que atributos nas tags `HTML`, podemos dá qualquer nome para prop, mas o ideal é que seja algo que faça sentido com o que essa prop vai representar na sua página. No caso da nossa aplicação teremos três botões e cada um vai apresentar um nome de uma tecnologia. Essa é a forma que podemos passar dinamicamente valores entre os nossos componentes, se precisarmos usar esse mesmo botão em alguma outra página com o valor de Angular por exemplo, poderíamos usá-lo assim: `<Button tech="Angular" />` e magicamente teríamos um botão com um valor diferente na nossa página.

