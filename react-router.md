# React Router

## O que é React Router?

Usamos rotas para navegar entre diferentes páginas\(estados\) de uma aplicação, quando precisamos desse fluxo no React podemos usar o pacote chamado `React Router` que resolve especificamente esse problema.

Vamos aproveitar parte do projeto que criamos na seção `React` e aplicar rotas nele, porém iremos realizar as seguintes alterações:

* Nossa aplicação agora terá quatro páginas: react, hooks, js e home;
* A página `home` vai conter três links onde cada um apontará para uma página diferente;
* Cada página terá um botão que volta pra página `home`;

Antes de iniciar as alterações acima vamos executar o comando abaixo para instalar o pacote do react-router:

```bash
npm install --save react-router-dom
```

## Usando o `<BrowserRouter />`

Após instalar a biblioteca de rotas temos acesso a diversos componentes disponíveis para criarmos nossas rotas. O primeiro componente que vamos usar é o `<BrowserRouter />` que é basicamente responsável por informar em que ponto da nossa aplicação inicia nossas rotas, vamos usá-lo no nosso componente `<App />` que sofreu algumas alterações conforme mostrado abaixo:

```javascript
import React from "react";
import { BrowserRouter } from "react-router-dom";

export const App = () => {
  return (
    <BrowserRouter>
      <div className="app">

      </div>
    </BrowserRouter>
  );
};
```

## Usando o `<Switch />` e o `<Route />`

Agora vamos importar o componente `<Switch />` que serve para controlar a troca de rotas e o `<Route />` para criar a própria rota, esse componente recebe alguns atributos, vamos falar sobre três específicos que usaremos na nossa aplicação:

1. `path`: recebe um texto que define a rota onde o componente será apresentado, então o caminho `path="/react"` referencia a página do react quando usarmos `/react` na nossa `url`.
2. `component`: recebe o componente que será apresentado no caminho que foi definido no `path`.
3. `exact`: usamos quando temos várias rotas iniciadas com o mesmo valor, no nosso caso temos a rota `/` que aponta pra página `home` porém as outras rotas também iniciam com `/`, para que o algoritimo aponte pra `home` apenas quando a rota for `/` precisamos usar a palavra reservada `exact`

```javascript
import React from "react";
import { BrowserRouter, Switch, Route } from "react-router-dom";

// aqui importamos nossas páginas
import { HooksPage } from "./HooksPage";
import { JsPage } from "./JsPage";
import { ReactPage } from "./ReactPage";
import { Home } from "./Home";

export const App = () => {
  return (
    <BrowserRouter>
      <div className="app">
        <Switch>
          {/* aqui definimos a rota e a page que será apresentada */}
          <Route path="/" exact component={Home} />
          <Route path="/hooks" component={HooksPage} />
          <Route path="/js" component={JsPage} />
          <Route path="/react" component={ReactPage} />
        </Switch>
      </div>
    </BrowserRouter>
  );
};
```

## Usando o `<Link />`

Com todas as rotas definidas e criadas, agora vamos usar outro componente chamado `<Link />`, ele recebe a propriedade `to` que recebe um texto como valor, esse valor precisa ser o mesmo definido no atribudo `path` da rota. Usaremos o `<Link />` na página `home` onde teremos os links que apontam para as outras páginas.

```javascript
import React from "react";

import { Message } from "./Message";
import { Link } from "react-router-dom";

export const Home = () => {
  return (
    <div>
      <Message name="World" />
      <nav className="nav">

         {/* aqui o link pra cada page */}
        <Link to="/react" className="nav-link">
          React
        </Link>
        <Link to="/js" className="nav-link">
          Javascript
        </Link>
        <Link to="/hooks" className="nav-link">
          Hooks
        </Link>
      </nav>
    </div>
  );
};
```

E por último temos um link em cada página que aponta pra `home` veja no exemplo da página  `hooks`   \[e aqui está o link da nossa aplicação\]\([https://codesandbox.io/s/hello-world-react-router-hl9yq?file=/src/App.js](https://codesandbox.io/s/hello-world-react-router-hl9yq?file=/src/App.js)\)

```javascript
import React from "react";
import { Link } from "react-router-dom";

import { Figure } from "./Figure";
import { Message } from "./Message";

import hooksImage from "./assets/img/hooks.png";

export const HooksPage = () => (
  <div>
    <Figure src={hooksImage} alt="Hooks" />
    <Message name="Hooks" />
    <Link to="/" className="nav-link">
      Go Home
    </Link>
  </div>
);
```

## Referências

* [Roteamento no React com os poderes do React Router v4](https://medium.com/collabcode/roteamento-no-react-com-os-poderes-do-react-router-v4-fbc191b9937d)
* [REACT – CONFIGURANDO ROTAS COM REACT-ROUTER](https://bognarjunior.wordpress.com/2018/03/31/react-configurando-rotas-com-react-router/)
* [React Router docs](https://reacttraining.com/react-router/)

