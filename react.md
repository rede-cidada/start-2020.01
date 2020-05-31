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

Para entendermos os próximos conceitos vamos criar juntas uma Pequena aplicação usando React.

### O que é componente?

As aplicações em React são baseadas em componentes que são pequenos blocos de códigos que podem ser reutilizados. Esses blocos são funções que podem receber dados de entrada como parâmetros e retornam um elemento React através do JSX e no final esses são transformados no DOM Virtual e mostrados na tela através do DOM.

Agora vamos tentar entender tudo isso através da nossa aplicação que conterá os seguintes componentes:

1. Componente `<Message />` que retorna um `<h1>` com uma mensagem.
2. Componente `<Figure />` que retorna um `<img>` com uma imagem.
3. Componente `<Button />` que retorna um `<button>` com um texto.
4. Componente `<App />` que retorna uma `<div>` com todos os componetes que criamos e na ordem que eles devem ser apresentados na tela.
5. Por fim teremos o `index.js` que terá o método para de fato renderizar nosso componente `<App/>` no DOM e fazer com que o usuário possa visualizar nossa aplicação.

### 1. Criando o componente`<Message />`

Como já falamos, componetes são funções que retornam um elemento `React`, então bora tentar criar uma função para representar nosso componente `Message`.

Antes de iniciar a desenvolver nosso componente vamos ter alguns pontos de atenção, não se preocupe se não entender todos os conceitos agora, iremos entrar em detalhes sobre todos mais tarde:

1. Todo componente React deve iniciar com a letra maiúscula.
2. Todo componente React precisa importar a função `React`.
3. No retorno do nosso componente, códigos javascript só funcionam se forem envolvidos por chaves.
4. Todo componente deve retornar um único elemento, então fazendo uma analogia com o que aprendemos no `HTML`, o retorno de um componente React não pode conter irmãos nesse caso devemos envolvê-lo em um outro elemento, ou seja, no retorno de um componente React todos elementos tem sempre um único `pai`, veja o exemplo abaixo:

- ```HTML
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

```JS
// Message.js
// importando o react
import React from "react";

// criando nosso componente
export const Message = () => <h1>Hello World React</h1>;
```

### 2. Usando o componente`<Message />`

Beleza, já temos nosso componente `Message`, agora em todas as páginas que a gente precisar mostrar essa mensagem é só importar nosso componente e usá-lo, veja o exemplo abaixo onde estamos usando ele no componente `App`:

```JS
// App.js
import React from "react";

// importando nosso componente
import { Message } from "./Message";

export const App = () => (
  <div className="App">

    {/* usando nosso componete */}
    <Message />
  </div>
);
```
