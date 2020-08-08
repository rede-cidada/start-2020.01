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

Introdução ao JavaScript - Exercício Aula 04   
[link do enunciado da questão](https://docs.google.com/document/d/1HNhwtypK1Lg6J2mMUXGl6WDXeyjqRZuvynHgvqG0QDY/edit)

Questão1

```javascript

// Criar uma condicional que verifica se tem saldo
//suficente para a compra do produto.

let preco = 100;
let valorDinheiro = 50;

if(valorDinheiro >=100){
    console.log('compra efetuada com sucesso')
}else{
    console.log('a grana tá curta.')
}
```

Questão 2

```javascript
let tempo= "nevando";

if (tempo === "nevando") {
  console.log("usar um casaco");
} else if (tempo === "chovendo") {
  console.log("usar uma jaqueta.");
} else {
  console.log("hoje o está bom para roupas leves");
}
```

Questão 3

```javascript

let diaSemana = 'segunda-feira';

switch(diaSemana){
    case 'segunda-feira':
    console.log('atividade física');
    break;
    
    case 'terca-feira':
    console.log('estudar Node')
    break;

    case 'quarta-feira':
        console.log('atividade física')
        break;

    case 'quinta-feira':
        console.log('faculdade')
        break;

    case 'sexta-feira':
        console.log('inglês')
        break;

    case 'sábado':
        console.log('Relaxar')
        break; 
        
     default:
         console.log('dia da semana inválido')   

}
```

