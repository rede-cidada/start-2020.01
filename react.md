# React

## O que é React e pra que serve?
Apesar de muitos confundirem o React não é um framework e sim uma biblioteca.

Tá. Mas qual a diferença entre framework e lib? — Framework é um conjunto de funções e módulos que resolvem vários problemas diferentes, por exemplo: o Angular resolve problemas de rotas e views ao mesmo tempo e mais uma porrada de outras necessidades... Diferentemente do React que foca em resolver o "problema" de renderização da View. Ué mas e se eu quiser usar rotas no React? — Simples, você terá que importar uma lib que resolve o problema de rota. 
> Palavras da Deva Laryssa Magalhães [nesse artigo aqui!](https://medium.com/@larymagal/react-para-iniciantes-f09360a24786)

React é uma biblioteca criada pelo Facebook e é usado basicamente para construir telas, tipo essa aqui que você está olhando. O legal é que ele constroi telas de forma declarativa, isso significa que basicamente declaramos como que a nossa tela vai reagir a um estado ou a como um dado se comporta. 

## O que é o Virtual DOM?
Antes de falar sobre virtual DOM vamos relembrar sobre o DOM. Vimos na sessão do DOM como alterar a nossa página adicionando, alterando ou removendo os elementos, porém esse processo de realizar essas mudanças diretamente no DOM causa lentidão para renderizar novamente o elemento por não ser um processo muito performático.

Virtual DOM é uma técnica que o React usa pra atualizar a tela onde é construido os dados a ser apresentado na tela, ele nada mais é que um objeto virtual que representa o DOM real, você pode ler [esse artigo](https://medium.com/roliveiradev/por-que-getelementbyid-deve-ser-evitado-6b0d35d055fe) que explica detalhadamente todo esse processo de DOM e Virtual Dom

## O que é JSX
Para construir o virtual DOM é preciso criar uma seequência de instruções pra manipular a árvore do DOM. Construir com javascript a estrutura do HTML é um processo bem complexo que você deve lembrar quando estudamos sobre a API do DOM. Por isso o time do React desenvolveu uma forma de escrever algo parecido com HTML porém que fosse traduzido facilmente para javascript, e isso é o JSX, ele tem uma estrutura muito parecida com HTML mas não é HTML, ele é convertido pra javascript que gera o virtual DOM.

Como consequência disso você não consegue utilizar algumas palavras que são reservadas do javascript, por exemplo o atributo ```class``` no JSX a gente usa a palavra ```className``` porque no javascript ```class``` é reservada pra criação de classes. Veja [nesse link](https://pt-br.reactjs.org/docs/dom-elements.html) todas as palavras que são reservadas no javascript e qual as palavras que usamos para representá-las no React.

## Conceito de Components
A principal característica do React é que ele é baseado em componentes que são pequenos blocos de códigos que podem ser reutilizados. Os componentes React são basicamente funções que podem receber dados de entrada e retornam elementos HTML através do JSX e assim esses são mostrados na tela. 

## Componente de função x componente de classe
A maneira mais simples de escrever um componente com React é escrever uma função que retorna um elemento React.

```JS
// exemplo de um componente de função
import React from "react";

// uma função
export const Hello = () => {

// que retorna um elemento React
return <h1>Hello React</h1>;
};
```

## Conceito de state
## Component com stateful
## Como criar  components e carregar em uma única página
## React dev tools
## Como posso criar minha primeira aplicação com React?
## Atividades práticas
