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

E como você pode ver, o primeiro elemento `<html>` no código é o nó mãe da árvore, enquanto os elementos `<head>` e `<body>` são nós filhos do nó mãe `<html>`. O `<title>` e os `<meta>` são filhos do elemento `<head>`, enquanto os elementos `<h1>` e o  `<p>` são nós filhos do elemento `<body>`. Se você já ouviu falar sobre a árvore genealógica em biologia, pense na árvore de objetos DOM como uma réplica semelhante da árvore genealógica

### Acessando o DOM <a id="How_Do_I_Access_the_DOM.3F"></a>

> Você não precisa fazer nada de especial para começar a usar o DOM, todo navegador usa um modelo de objeto de documento para tornar as páginas da web acessíveis via JavaScript.

#### 

#### Métodos de acesso DOM

O DOM possui muitos métodos, são eles que fazem a ligação entre os nodes \(elementos\) e os eventos. Vamos estudar os métodos mais usados lembrando que existem muitos outros e você pode ver todos [nesse link](https://developer.mozilla.org/en-US/docs/Web/API/Document).

```
$ give me super-powers
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

{% code title="hello.sh" %}
```bash
# Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```
{% endcode %}



