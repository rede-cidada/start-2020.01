# Solução Exercícios - JavaScript

Introdução ao JavaScript - Exercício Aula 01 

            O objetivo da atividade é colocar em prática os conceitos abordados na aula.

* introdução ao javascript 
* Interatividade com os métodos nativos da linguagem
* sintaxe
* tipos de dados 

1\) Declare uma variável e mostre no console do navegador

```javascript
let nome = 'Patricia';
console.log(nome);
```

2\) Declare outra variável e mostre com um alerta no navegador

```javascript
let fruta = 'Banana';
alert(fruta);
```

3\) let mensagem = 'Clique em um dos botões abaixo:'; confirm\(mensagem\);

```javascript
let mensagem = 'Clique em um dos botões abaixo:';
confirm(mensagem);
```

4\)Declare uma variável e mostre no console do navegador somente se essa variável for uma string.

```javascript
let nomeVariavel = 10;

if (typeof nomeVariavel === 'number') {
  console.log(nomeVariavel); 
  // essa mensagem só aparece se a minha variável for do 
  //tipo string
};
```

Introdução ao JavaScript - Exercício Aula 02   
[link do enunciado da questão](https://docs.google.com/document/d/1_8GylSjueFnN1H_GjNQL8G0pBKXdAGXQ3KFLpyWpiVM/edit?usp=sharing)



```javascript

/*
Criar um arquivo .html e um arquivo externo .js
Fazer a chamada do arquivo .js  no index.html.
no arquivo .js declare três variáveis e capture a entrada dos dados do usuário.
Combine a entrada com outras palavras para criar uma história ou frase.
Exiba a história no elemento <p> dentro do elemento <main>.

*/
//variavel adjetivo, que está sendo atribuido o método prompt
const adjetivo = prompt('digite um adjetivo');

//variavel verbo, que está sendo atribuido o método prompt
const verbo = prompt('digite um substantivo');

//variavel substantivo, que está sendo atribuido o método prompt
const substantivo = prompt('digite um verbo');


//variável frase ela está armazenando as variáveis acima, que tem o objetivo de formar a frase
const frase = `<p>O programa StartLatam ${adjetivo} e ${verbo} muitas ${substantivo}</p> `

document.querySelector('main').innerHTML = frase;
```

