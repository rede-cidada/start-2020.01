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
import React from 'react' // importando o react

// exemplo de um componente de função usando JSX
const Hello = (props) => {
  return <h1 className="title">Hello {props.name}!</h1>
}

// o mesmo componente acima sem o uso do JSX
const Hello = (props) => {
  return React.createElement(
    'h1', // o elemento que vai virar HTML
    {
      className: 'title', // os atributos são passados nesse objeto
    },
    'Hello ', // aqui vai o conteúdo de texto que ficará dentro do HTML
    props.name, // aqui como é separado o javascript
    '!' // aqui o restante do conteúdo de texto
  )
}
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

Aplicando a teoria acima na nossa aplicação, vamos usar o método `ReactDOM.render()` no arquivo `index.js` que é o primeiro arquivo a ser executado quando uma aplicação é inicializada, veja como utilizamos a chamada no exemplo abaixo:

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
import React from 'react' // importando o react
import reactImg from './assets/img/react.png' // importando a imagem

// criando o cmponente <Figure/>
export const Figure = () => <img className="image" src={reactImg} />
```

Só um ponto de atenção de como a gente usa imagens no `React`, ela precisa ser importada recebendo um nome, que seria uma variável que vai representar o caminho da imagem, depois usamos essa `variável` no atributo `src` da tag `img`. Note que o valor repassado para o atributo deve ser entre chaves`{}`, já que se trata de um conteúdo `javascript` sendo utilizado dentro do `JSX`.

### 6. O que é `Props` no React?

`Props` é a abreviação pra propriedades e são representadas por um objeto. É a forma que usamos para compartilhar informações entre os componentes React. Para entender melhor esse conceito vamos criar o componente `<Button />` da nossa aplicação:

```javascript
import React from 'react' // importando o react

// criando o cmponente <Button/>
// repare que agora nosso componente recebe um parâmetro que chamamos de `props`
// poderíamos dá qualquer nome, estamos usando a palavra "props" só por padrão mesmo
// estamos usando a propriedade chamada "tech" que foi um nome também que
// escolhemos pra representar o valor apresentado em cada botão
export const Button = (props) => <button className="btn">{props.tech}</button>
```

Agora vamos usar esse componente que criamos lá no nosso `<App />`

```javascript
import React from 'react'
import { Message } from './Message'
import { Figure } from './Figure'
import { Button } from './Button' // importando nosso componente <Button />

export const App = () => (
  <div className="app">
    <Figure />

    {/* criando uma prop chamada "name" */}
    <Message name="React" />

    <div className="btn-groups">
      {/* usando nosso componente e criando uma prop chamada "tech" */}
      <Button tech="React" />
      <Button tech="Javascript" />
      <Button tech="JSX" />
    </div>
  </div>
)
```

Alterando nosso componente `<Message />` para receber a prop `name`:

```jsx
import React from "react";

// recebendo a prop como parâmetro
export const Message = props => (

  {/* usando o valor passado na prop "name" */}
  <h1 className="message">Hello {props.name}!</h1>
);
```

Se você prestar atenção vai ver que usamos as props da mesma forma que atributos nas tags `HTML`, podemos dá qualquer nome para prop, mas o ideal é que seja algo que faça sentido com o que essa prop vai representar na sua página. No caso da nossa aplicação teremos três botões e cada um vai apresentar um nome de uma tecnologia. Essa é a forma que podemos passar dinamicamente valores entre os nossos componentes, se precisarmos usar esse mesmo botão em alguma outra página com o valor de Angular por exemplo, poderíamos usá-lo assim: `<Button tech="Angular" />` e magicamente teríamos um botão com um valor diferente na nossa página.

Podemos acessar a prop no componente recebendo elas por parâmetros nos componentes de função ou através do `this.props` no componente de classe. As props não se limitam a receber apenas strings, podemos passar qualquer tipo de valor pra ela, como array, objeto, função, número ou seja, qualquer valor que precisarmos compartilhar.

Props possuem valores estáticos que são passados hierarquicamente do "pai" para o "filho" e não são alterados. No nosso exemplo o componente pai seria o `<App />` e não conseguimos passar um dado do componente `<Message />` para ele por exemplo.

### 7. Componente de função x componente de classe?

Até agora todos os componentes que criamos são componentes de função e tem um motivo por trás de tudo isso, se você prestar atenção, até agora só criamos componentes que mostram algo na tela, algo que nunca muda, algo que o usuário não interage escrevendo, clicando ou tentando alterar qualquer coisa na nossa aplicação. Esse é a responsabilidade de um componente de função, ele é usado pra criar componentes estáticos e que não tem alteração após apresentar os dados na página.

Os componentes de função também são chamados de Stateless Components, ou componentes sem estado. Os componentes de classe também são chamados de Stateful Components, ou componentes com estados.

#### O que muda num componente de classe?

Componente de classe é representado em javascript por uma classe, ele deve estender `Componente` do pacote `React`. Quando criamos um componente de classe temos acesso a vários métodos da biblioteca React, sendo que somente o método `render()` é obrigatório.

Componentes de classe é útil quando precisamos alterar algo na página após o conteúdo ser apresentado. No nosso exemplo, vamos realizar as seguinte mudanças:

* Mudar o componente `<App />` para que agora seja um componente de class.
* Mudar o componente `<Message />` para que agora ele receba uma `prop` que vai substituir o nome da tecnologia, a mensagem agora ficaria: `Hello {props.tech}`.
* Adicionar um estado no componente `<App />` que vai gerenciar a mudança da tecnologia passada na mensagem.
* Adicionar uma função no componente `<Button />` que vai receber a seguinte ação: quando o usuário clicar no botão a mensagem mostrará: `Hello + tecnologia do botão clicado`.

Transformando nosso componente `<App />` em um componente de classe:

```javascript
import React, { Component } from 'react' // agora importamos também o Component
import { Message } from './Message'
import { Figure } from './Figure'
import { Button } from './Button'

// aq alteramos nossa função pra uma classe
export class App extends Component {
  // chamamos o método render que é obrigatório para componente de classe
  render() {
    //  aqui continua tudo como era antes...
    return (
      <div className="app">
        <Figure />
        <Message name="React" />
        <div className="btn-groups">
          <Button tech="React" />
          <Button tech="Javascript" />
          <Button tech="JSX" />
        </div>
      </div>
    )
  }
}
```

### 8. O que é `state` o React?

Diferente das `props`, o `state` ou `estado` não é repassado ao componente e sim configurado dentro dele. Pense no estado como as propriedades de nossa classe que devem ser armazenadas para renderizarmos o componente da forma correta. Os estados só podem existir em componentes de classe e seus valores podem ser alterados, essas mudanças de valores são gerenciados pro vários métodos disponíveis em um componente do tipo classe e são guardados dentro da classe em um objeto usando essa sintaxe `state= {chave: 'valor'}`.

Vamos tentar aplicar esse conceito à nossa aplicação, vamos alterar o componente `<Message />` para receber a prop name, e o valor dessa prop será repassado pelo state da classe `<App />`, ficou meio confuso, mas tente entender as palavras acima examinando as mudanças no código abaixo:

```javascript
import React, { Component } from 'react'
import { Message } from './Message'
import { Figure } from './Figure'
import { Button } from './Button'

export class App extends Component {
  // aqui criamos um estado
  state = {
    value: 'React',
  }

  render() {
    return (
      <div className="app">
        <Figure />

        {/* agora usamos o valor do estado para repassar para o componente <Message /> */}
        <Message name={this.state.value} />
        <div className="btn-groups">
          <Button tech="React" />
          <Button tech="Javascript" />
          <Button tech="JSX" />
        </div>
      </div>
    )
  }
}
```

Para acessar os valores do nosso estado usamos a variável `this.state.nome_da_propriedade`, no nosso exemplo acima, criamos uma propriedade chamada `value` \(que poderia ser qualquer nome\) e essa propriedade recebe o valor `React`, então em qualquer parte do código que eu precise usar esse valor eu posso acessá-lo assim: `this.state.value`

### 9. Alterando o estado do nosso componente `<App />`

Estamos quase no final da construção da nossa aplicação, o que precisamos fazer é:

1. Quando um botão for clicado
2. A mensagem irá alterar para `Hello + o nome do botão clicado`
3. Então se clicarmos em `JSX`
4. A mensagem será: `Hello JSX`

Para fazer a ação acima vamos realizar as alterações abaixo no nosso componente `<App />`:

* Criar uma função que recebe como parâmetro o valor do botão clicado;
* Dentro dessa função alterar o valor do estado `value`, que agora receberá o valor desse botão;
* Passar essa função como prop para o componente `<Button />`;
* Usar essa prop no evento `onClick` do componente `<Button />`;

O React não permite alterar o estado de um componente da mesma forma que alteramos uma variável comum, isso porque o estado é imutável, ou seja, ele nunca deve ser alterado e sempre deve ser sobreposto, pra isso o React tem a função `this.setState({ propriedade: valor})`, onde a propriedade é nome da propriedade que queremos alterar no nosso estado e o valor é a nova informação que queremos repassar para nossa propriedade.

Aplicando o conceito acima no nosso componente `<App />`:

```javascript
import React, { Component } from "react";
import { Message } from "./Message";
import { Figure } from "./Figure";
import { Button } from "./Button";

export class App extends Component {
  state = {
    value: "React"
  };

  // aqui estamos criando a nova função que recebe como parâmetro o valor do botão clicado
  // e no retorno da função estamos alterando a propriedade "value"
  handleClickTechnology = techName => this.setState({ value: techName });

  render() {
    return (
      <div className="app">
        <Figure />
        <Message name={this.state.value} />
        <div className="btn-groups">
          <Button
            tech="React"
            {/* aqui estamos criando uma propriedade para o <Button /> que recebe como valor nossa função*/}
            handleClickTechnology={() => this.handleClickTechnology("React")}
          />
          <Button
            tech="Javascript"
            handleClickTechnology={() =>
              this.handleClickTechnology("Javascript")
            }
          />
          <Button
            tech="JSX"
            handleClickTechnology={() => this.handleClickTechnology("JSX")}
          />
        </div>
      </div>
    );
  }
}
```

Chamando a função no `<Buttom />` através da nova propriedade:

```javascript
import React from "react";

export const Button = props => (
  {/* aqui estamos passando a prop no evento onClick do botão*/}
  <button className="btn" onClick={props.handleClickTechnology}>
    {props.tech}
  </button>
);
```

Prontinho, agora temos uma pequena aplicação com os conceitos básicos do React, agora sua atividade é criar qualquer coisa usando os conceitos aplicado aqui para praticar tudo o que foi passado, você pode acessar o [código completo aqui](https://codesandbox.io/s/hello-world-react-blc7h?file=/src/Button.js:0-158)

## Listas e `keys` no React

Ainda olhando pra nossa aplicação, o componente `<Button />` é chamado 3x no componente `<App />`, vamos fazer as alterações abaixo pra aplicar os conceitos de listas no React:

* Criar uma nova propriedade no estado da classe lista que vai receber um array de tecnologias
* Usar o método `map` do javascript pra interar esse array retornando pra cada item um componente `<Button />` que receberá o valor do array como valor da prop `tech`.

Quando usamos uma lista no retorno de componente React é necessário passar uma `key` para cada item da lista. Ela é um atributo string especial que ajuda o React a identificar qual item da lista foi alterado, adicionado ou removido. A `key` deve ser atribuída ao item dentro do array que está sendo manipulado, para dar uma identidade estável aos elementos e ela deve ser única.

Vejamos abaixo como ficaram essas alterações:

```javascript
import React, { Component } from "react";
import { Message } from "./Message";
import { Figure } from "./Figure";
import { Button } from "./Button";

export class App extends Component {
  state = {
    value: "React",
    techs: ["React", "Javascript", "JSX"] // criamos um novo estado
  };

  handleClickTechnology = techName => this.setState({ value: techName });

  render() {
    return (
      <div className="app">
        <Figure />
        <Message name={this.state.value} />

        <ul className="btn-list">

          {/* para cada item do array do nosso estados retornamos um novo componente <Button /> */}
          {this.state.techs.map(tech => (

            {/* passamos o valor do array para a key */}
            <li className="btn-item" key={tech}>
              <Button
                tech={tech} {/* passamos o valor do array para o botão através da prop tech */}
                handleClickTechnology={() => this.handleClickTechnology(tech)} {/* passamos o valor do array para a prop que passará para o evento click do botão */}
              />
            </li>
          ))}
        </ul>

      </div>
    );
  }
}
```

## Ciclos de vida de um componente

Podemos dizer que um ciclo de vida de um componente inicia quando ele é montado na tela, sofre algumas alterações e depois ele é desmontado. Um componente de classe possui vários métodos especiais para gerenciar o ciclo de vida de um componente, não vamos entrar em detalhes sobre eles nesse tutorial mas você pode ler mais sobre [nesse artigo.](https://blog.rocketseat.com.br/react-do-zero-ciclo-de-vida-stateless-components-e-arquitetura-flux/).

Abaixo uma imagem dos métodos utilizados para manipular o ciclo de vida de um componente React.

![Fases e m&#xE9;todos do ciclo de vida de um componente em React.](.gitbook/assets/image%20%286%29.png)

## O que é React Hooks?

Hooks são um conjunto de novas funcionalidades adicionadas ao React a partir da versão 16.8. Uma das novidades é que agora conseguimos manipular estados em componente de função usando `Hooks` e de uma forma mais simples do que o que vimos acima nos componentes de classe.

Os Hooks são classificados em básicos e adicionais da seguinte forma:

Hooks básicos:

* useState
* useEffect
* useContext

Hooks adicionais:

* useReducer
* useCallback
* useMemo
* useRef
* useImperativeMethods
* useMutationEffect
* useLayoutEffect

### Transformando nosso componente `<App />` em um componente de classe e usando o `useState`

Veja abaixo como ficou nosso componente usando `hooks`, [aqui está o novo código com as alterações](https://codesandbox.io/s/hello-world-react-hooks-qxpnh?file=/src/App.js).

```javascript
import React, { useState } from "react"; // agora usando o hook useState
import { Message } from "./Message";
import { Figure } from "./Figure";
import { Button } from "./Button";

// transformamos nosso componente em uma função
export const App = () => {
  // esse estado virou um simples array
  const techs = ["React", "Javascript", "JSX"];

  // aqui temos uma variável pra representar o valor que vai ser alterado
  // e uma função para realizar a alteração do estado
  const [value, setValue] = useState(techs[0]);

  const handleClickTechnology = techName => setValue(techName); // usando a função que criamos para alterar o estado

  return (
    <div className="app">
      <Figure />

      <Message name={value} /> {/* aqui passamos o valor do estado que será alterado */}
      <ul className="btn-list">

        {/* aqui só removemos o this.state */}
        {techs.map(tech => (
          <li className="btn-item" key={tech}>
            <Button
              tech={tech}
              handleClickTechnology={() => handleClickTechnology(tech)} {/* aqui só removemos o this */}
            />
          </li>
        ))}
      </ul>
    </div>
  );
};
```

## Referências

* [reprograma/T7-react-I](https://github.com/reprograma/T7-react-I)
* [pt-br.reactjs.org/docs](https://pt-br.reactjs.org/docs/hello-world.html)
* [Learn React by creating a comment app](https://www.qcode.in/learn-react-by-creating-a-comment-app/)
* [Métodos do ciclo de vida de componentes ReactJS — Um mergulho profundo!](https://medium.com/creditas-tech/m%C3%A9todos-do-ciclo-de-vida-de-componentes-reactjs-um-mergulho-profundo-332ed7b3b782)
* [O Guia Completo do React e o seu Ecossistema](https://medium.com/tableless/o-guia-completo-do-react-e-o-seu-ecossistema-b31a10ecd84f)
* [React Hooks Cheatsheet](https://react-hooks-cheatsheet.com/)
* [REACT – HOOKS ENTENDENDO O CONCEITO.](https://bognarjunior.wordpress.com/2018/11/04/react-hooks-entendendo-o-conceito/)
* [Ganchos? Vamos conversar sobre React hooks](https://blog.getty.io/ganchos-vamos-conversar-sobre-react-hooks-1d4309e7b4c0)

