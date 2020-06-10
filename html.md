# HTML

## Introdução ao HTML

Bem-vindo ao mundo do código! Por quê? HTML é o esqueleto de todas as páginas da web. Geralmente é o primeiro idioma aprendido por desenvolvedores, profissionais de marketing e designers e é essencial para o trabalho de desenvolvimento front-end. Se esta é a primeira vez que você está vendo um código, fique animado porque você pode criar coisas incríveis.

Então, o que exatamente é **HTML?** O HTML fornece estrutura para o conteúdo exibido em um site, como _**imagens**_, _**texto**_ ou _**vídeos**_. Clique com o botão direito do mouse em qualquer página da Internet, escolha _**"Inspecionar"**_ e você verá HTML em um painel da tela.

HTML significa HyperText Markup Language:

* Uma linguagem de _marcação_ é uma linguagem de computador que define a estrutura e a apresentação do texto bruto.
* Em HTML, o computador pode interpretar _o texto bruto_ envolvido em elementos HTML.
* _HyperText_ é o texto exibido em um computador ou dispositivo que fornece acesso a outro texto por meio de links, também conhecidos como _hiperlinks_ .

‌

**Propósito da Linguagem de marcação HTML.**

* Ser compreendida independente do dispositivo que vai ser acessado, o HTML é o mesmo para todos.
* Fácil compreensão
* Interoperabilidade - \( não há uma especificidade da linguagem de uma empresa para outra\)

Aprender HTML é o primeiro passo na criação de sites, mas mesmo um pouco de conhecimento pode ajudá-lo a inserir trechos de código em boletins, blogs ou modelos de sites. À medida que você continua aprendendo, é possível colocar em camadas HTML com CSS e JavaScript para criar sites dinâmicos e atraentes. Mas, por enquanto, vamos nos concentrar em como adicionar e modificar o conteúdo básico de uma página, como texto, imagens e vídeos. Não se preocupe se os sites parecerem feios - estamos apenas começando.

‌

## Anatomia do HTML

![https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz\_%2F-M7rYDNp\_MyRgjGoq0hu%2F-M7rYf3D1Pr8hlSSfZD9%2FCaptura de Tela 2020-05-21 a&#x300;s 11.06.14.png?alt=media&amp;token=a7022673-e688-478f-a116-63430326ac78](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7rYDNp_MyRgjGoq0hu%2F-M7rYf3D1Pr8hlSSfZD9%2FCaptura%20de%20Tela%202020-05-21%20a%CC%80s%2011.06.14.png?alt=media&token=a7022673-e688-478f-a116-63430326ac78)



HTML é composto de _elementos_ . Esses elementos estruturam a página da web e definem seu conteúdo. Vamos dar uma olhada em como eles são escritos.

A imagem acima apresenta um elemento de parágrafo HTML. Como podemos ver, o elemento de parágrafo é composto de:

* Uma _tag de abertura_ \( `<p>`\)
* O conteúdo \(texto "Hello World!"\)
* Uma _tag de fechamento_ \( `</p>`\)

Uma _tag_ e o _conteúdo_ entre elas são chamados de elementos HTML. Existem muitas tags que podemos usar para organizar e exibir texto e outros tipos de conteúdo, como imagens.

Vamos revisar rapidamente cada parte do elemento representado:

* _**Elemento HTML**_ \(ou simplesmente elemento\) - uma unidade de conteúdo em um documento HTML formado por tags HTML e o texto ou mídia que ele contém.
* _**Tag HTML**_ - o nome do elemento, cercado por um colchete de ângulo de abertura \( `<`\) e fechamento \( `>`\).
* _**Tag de abertura**_ - a primeira tag HTML usada para iniciar um elemento HTML. O tipo de tag é cercado por aberturas de abertura e fechamento de ângulo.
* _**Conteúdo**_ - as informações \(texto ou outros elementos\) contidas entre as tags de abertura e fechamento de um elemento HTML.
* _**Tag de fechamento**_ - a segunda tag HTML usada para finalizar um elemento HTML. As tags de fechamento têm uma barra \( `/`\) dentro delas, logo após o colchete angular esquerdo.



### Body Element

Um dos principais elementos HTML que usamos para criar uma página da web é o elemento _body_ . Somente o conteúdo dentro das tags do corpo de abertura e fechamento pode ser exibido na tela. Veja como são as tags corporais de abertura e fechamento. Depois que o arquivo tem um corpo, muitos tipos diferentes de conteúdo - incluindo texto, imagens e botões - podem ser adicionados ao corpo.



```markup
<body>
    <p>Curso de Front-End</p>
</body>

```

‌

## Estrutura HTML

O HTML é organizado como uma coleção de relacionamentos de árvore genealógica. Como você viu no último exercício, colocamos `<p>`tags nas `<body>`tags. Quando um elemento está contido dentro de outro elemento, ele é considerado _filho_ desse elemento. Diz-se que o elemento filho está _aninhado_ dentro do elemento _pai_ .

```markup
<body> 
  <p> Este parágrafo é um filho do corpo </p> 
</body>

```

No exemplo acima, o `<p>`elemento está aninhado dentro do `<body>`elemento. O `<p>`elemento é considerado um filho do `<body>`elemento e o `<body>`elemento é considerado o pai. Você também pode ver que adicionamos dois espaços de recuo \(usando a barra de espaço\) para melhor legibilidade.

Como pode haver vários níveis de aninhamento, essa analogia pode ser estendida aos netos, bisnetos e outros. O relacionamento entre os elementos e seus elementos ancestrais e descendentes é conhecido como _hierarquia_ .

Vamos considerar um exemplo mais complicado que usa algumas novas tags:

```markup
<body> 
  <div> 
    <h1>Irmão para p, mas também neto do corpo </h1> 
    <p>Irmão para h1, mas também neto do corpo </p> 
  </div> 
</body>

```

‌

Neste exemplo, o `<body>`elemento é o pai do `<div>`elemento. Os elementos `<h1>`e `<p>`são filhos do `<div>`elemento. Como os elementos `<h1>`e `<p>`estão no mesmo nível, eles são considerados irmãos e são netos do `<body>`elemento.

A compreensão da hierarquia HTML é importante porque os elementos filho podem herdar comportamento e estilo do elemento pai. Você aprenderá mais sobre a hierarquia de páginas da web quando começar a explorar o CSS.

Adicione um paragrafo como filho do elemento div e neto do elemento body.

```markup
<body>
  <h1>Hello World</h1>
  <div>
    <p>
      Este parágrafo é filho do elemento div e neto do elemento body.
    </p>
  </div>  
</body>

```

‌

### Headings

Os títulos em HTML são semelhantes aos de outros tipos de mídia. Por exemplo, nos jornais, títulos grandes são normalmente usados ​​para capturar a atenção do leitor. Outras vezes, os títulos são usados ​​para descrever o conteúdo, como o título de um filme ou um artigo educacional.

O HTML segue um padrão semelhante. No HTML, existem seis _títulos_ diferentes , ou _elementos de título_ . Os títulos podem ser usados ​​para uma variedade de finalidades, como seções de títulos, artigos ou outras formas de conteúdo.

A seguir, é apresentada a lista de elementos de cabeçalho disponíveis em HTML. Eles são pedidos do maior para o menor em tamanho.

`<h1>`- usado para títulos principais. Todos os outros títulos menores são utilizados para subtítulos.`<h2><h3><h4><h5><h6>`

O código de exemplo a seguir usa um título destinado a capturar a atenção do leitor. Ele usa o maior cabeçalho disponível, o principal elemento de cabeçalho:

```yaml
<h1>BREAKING NEWS</h1>

```

‌

## Divs

Um dos elementos mais populares em HTML é o `<div>`elemento `<div>`é a abreviação de "divisão" ou um contêiner que divide a página em seções. Essas seções são muito úteis para agrupar elementos em seu HTML.

```markup
<body> 
  <div> 
    <h1>Por que usar divs?</h1> 
    <p>Ótimo para agrupar elementos!</p> 
  </div> 
</body>

```

`<div>`s podem conter qualquer texto ou outros elementos HTML, como links, imagens ou vídeos. Lembre-se de sempre adicionar dois espaços de recuo ao aninhar elementos dentro de `<div>`s para melhor legibilidade.

## Atributos

Se queremos expandir tag de um elemento, podemos fazê-lo usando um _atributo_ . Os atributos são conteúdo adicionado à tag de abertura de um elemento e podem ser usados ​​de várias maneiras diferentes, desde o fornecimento de informações até a alteração do estilo. Os atributos são compostos das duas partes a seguir:

* O _**nome**_ do atributo
* O _**valor**_ do atributo

Vamos conhecer os atributos mais usados no dia a dia de um desenvolvedor, mas tem vários atributos que não vamos listar aqui, mas vamos deixar link para consulta.

O atributo **`id`**. Podemos usar para especificar apenas um elemento html .

Quando adicionamos um `id`a uma  **`<div>`**, colocamos na tag de abertura:

```markup
<div id="intro"> 
  <h1>Introdução</h1> 
</div>

```

Com o atributo **`class`** permite atribuir formatação a VÁRIOS elementos de uma vez só.

```markup
<div class="intro"> 
  <h1>Introdução</h1> 
  <h3>Curso de Front-End Developer</h3> 
</div>

```

O atributo **`href`**, especifica a URL de um link no elemento &lt;a&gt;

```markup
<a href="<http://www.redecidada.org.br/>">Site Rede Cidadã</a>

```

O elemento `<a>`elemento âncora é usado para criar hiperlinks em um documento HTML. Os hiperlinks podem apontar para outras páginas da web, arquivos no mesmo servidor, um local na mesma página ou qualquer outro URL por meio do atributo de referência do hiperlink `href`.

```markup
<!--Ligando um texto--> 
<a href="<http://www.redecidada.org.br/>">Visite este site</a> 
<!--Vincular uma imagem --> 
<a href="<http://www.redecidada.org.br/>"> 
<img  src="logo.jpg">Clique nesta imagem</a>

```

### Link para parte diferente da página \#.

O elemento âncora `<a>`pode criar hiperlinks para diferentes partes do mesmo documento HTML usando o `href`atributo para apontar para o local desejado `#`seguido pelo `id`elemento do qual o link será vinculado.

```markup
<div> 
  <p id="id-do-elemento-para-link-para">Uma parte diferente da página!</P> 
</div> 
<a href="#id-de-element-a-link-a">Leve-me para uma parte diferente da página</a>

```

### Target

O atributo`target` em um `<a>`elemento âncora especifica onde um hiperlink deve ser aberto. Um `target`valor de `"_blank"`dirá ao navegador para abrir o hiperlink em uma nova guia

```markup
<a href="<http://www.redecidada.org.br/>" target="_blank">Visite este site</a> 

```

```markup
<img src="nome_imagem.jpg"/>

```

O atributo **`src`** URL de um conteúdo, pode ser uma imagem, video. atributo deve ser definido como a _fonte_ da imagem ou o local da imagem, Neste caso, o valor `src`deve ser o _Uniform Resource Locator_ \(URL\) da imagem. Um URL é o endereço da Web ou o endereço local em que um arquivo está armazenado.

O atributo _**`alt`**_ especifica um texto alternativo caso uma imagem não possa ser exibida. significa texto alternativo, traz significado às imagens em nossos sites. O `alt`atributo pode ser adicionado à tag da imagem exatamente como o `src`atributo. O valor de `alt`deve ser uma descrição da imagem.

O `alt`atributo também serve aos seguintes propósitos:

* Se uma imagem não carregar em uma página da web, o usuário pode passar o mouse sobre a área originalmente destinada à imagem e ler uma breve descrição da imagem.
* Usuários com deficiência visual geralmente navegam na Web com o auxílio de um software de leitura de tela. Quando você inclui o `alt`atributo, o software de leitura de tela pode ler a descrição da imagem em voz alta para o usuário com deficiência visual.
* O `alt`atributo também desempenha um papel na Otimização de mecanismos de pesquisa \(SEO\), porque os mecanismos de pesquisa não podem "ver" as imagens nos sites enquanto pesquisam na Internet. Ter `alt`atributos descritivos pode melhorar a classificação do seu site.

```markup
<img src="foto_perfil.jpg" alt="foto_perfil"/>

```

‌

## Listas não ordenadas

Além de organizar o texto em forma de parágrafo, você também pode exibir o conteúdo em uma lista de fácil leitura.

Em HTML, você pode usar uma tag de _lista não ordenada_ \( `<ul>`\) para criar uma lista de itens em nenhuma ordem específica. Uma lista não ordenada descreve _itens de lista_ individuais com um marcador.

O `<ul>`elemento não deve conter texto bruto e não formatará automaticamente o texto bruto em uma lista não ordenada de itens. Itens de lista individuais devem ser adicionados à lista não ordenada usando a `<li>`tag A `<li>`tag do item ou da lista é usada para descrever um item em uma lista.

```markup
<ul> 
  <li>Home</li> 
  <li>Sobre mim</li> 
  <li>Contato</li> 
</ul>

```

No exemplo acima, a lista foi criada usando a `<ul>`tag e todos os itens de lista individuais foram adicionados usando a tag`<li>`

* Home
* Sobre mim
* Contato

## Listas ordenadas

_As listas ordenadas_ \( `<ol>`\) são como listas não ordenadas, exceto que cada item da lista é numerado. Eles são úteis quando você precisa listar etapas diferentes em um processo ou classificar itens do primeiro ao último.

Você pode criar a lista ordenada com a `<ol>`tag e adicionar itens de lista individuais à lista usando a tag `<li>`

```markup
<ol> 
  <li> Pré-aqueça o forno a 350 graus. </Li> 
  <li> Misture a farinha de trigo integral, bicarbonato de sódio, e sal. </li> 
  <li> Bata a manteiga, o açúcar em uma tigela separada. </Li> 
  <li> Adicione os ovos eo extrato de baunilha para uma tigela. </li> 
</ol>

```

A saída terá a seguinte aparência:

Pré-aqueça o forno a 350 graus.Misture a farinha de trigo integral, o bicarbonato de sódio e o sal.Bata a manteiga, o açúcar em uma tigela separada.Adicione os ovos e o extrato de baunilha à tigela.

## Imagens

Todos os elementos que você aprendeu até agora \(títulos, parágrafos, listas e extensões\) compartilham uma coisa em comum: eles são compostos inteiramente de texto! E se você quiser adicionar conteúdo à sua página da Web que não seja composto de texto, como imagens?

A `<img>`tag permite adicionar uma imagem a uma página da web. A maioria dos elementos requer tags de abertura e fechamento, mas a `<img>`tag é _de fechamento automático_ . Observe que o final da `<img>`tag possui uma barra `/`. As tags de fechamento automático podem incluir ou omitir a barra final - ambas serão renderizadas corretamente.

```markup
<img src="image-location.jpg"/>

```

‌

## Vídeos

Além de imagens, o HTML também suporta a exibição de vídeos. Como a tag `<img>`, a tag `<video>` requer um atributo `src` com um link para a fonte de vídeo. Diferentemente da `<img>`tag, no entanto, o `<video>`elemento requer uma tag de abertura e de fechamento.

```markup
<video src="myVideo.mp4"  width="320"  height="240"  controls>
  Vídeo não suportado 
</video>

```

Neste exemplo, a fonte de vídeo \( `src`\) é `myVideo.mp4`A fonte pode ser um arquivo de vídeo hospedado ao lado da sua página da web ou um URL que aponta para um arquivo de vídeo hospedado em outra página da web. Após o `src`atributo, os atributos `width`e `height`são usados ​​para definir o tamanho do vídeo exibido no navegador. O `controls`atributo instrui o navegador a incluir controles básicos de vídeo: pausar, reproduzir e pular.

O texto, “Vídeo não suportado”, entre as tags de abertura e fechamento do vídeo, será exibido apenas se o navegador não conseguir carregar o vídeo.

## Preparando para HTML

Agora que aprendemos sobre alguns dos elementos HTML mais comuns, é hora de aprender a configurar um arquivo HTML.

Os arquivos HTML requerem certos elementos para configurar o documento corretamente. Podemos informar aos navegadores da web que estamos usando HTML iniciando nosso documento com uma _declaração de tipo de documento_ .

A declaração é assim:

```markup
<!DOCTYPE html>

```

Esta declaração é uma instrução e deve ser a primeira linha de código no seu documento HTML. Ele informa ao navegador que tipo de documento esperar, juntamente com qual versão do HTML está sendo usada no documento. Por enquanto, o navegador assumirá corretamente que o `html`in `<!DOCTYPE html>`está se referindo ao HTML5, pois é o padrão atual. O código HTML é sempre salvo em um arquivo com uma extensão **.html** .

‌

## A tag &lt;html&gt;

A `<!DOCTYPE html>`declaração fornece ao navegador duas informações \(o tipo de documento e a versão HTML esperada\), mas na verdade não adiciona nenhuma estrutura ou conteúdo HTML.

Para criar estrutura e conteúdo HTML, precisamos adicionar `<html>`tag de abertura e fechamento após declarar `<!DOCTYPE html>`:

```markup
<!DOCTYPE html> 
<html> 
  <body>
    <!-- Conteúdo do site, aparece dentro da tag body-->
  </body>
</html>

```

Qualquer coisa entre as tag de abertura `<html>`e fechamento `</html>`será interpretada como código HTML. Sem essas tag, é possível que os navegadores interpretem incorretamente seu código HTML.

‌

## A Tag Head

Até agora, você fez duas coisas para configurar o arquivo corretamente.

* Declarou ao navegador que seu código é HTML com `<!DOCTYPE html>`
* Adicionado o elemento HTML \( `<html>`\) que conterá o restante do seu código.
* A tag `body` onde o conteúdo do nosso site ficará visível no navegador.

Adicionamos esses elementos a uma página que vamos criar na aula de hoje, mas precisamos também fornecer ao navegador algumas informações sobre a própria página. Podemos fazer isso adicionando a tag `<head>`

A `<head>`elemento faz parte do HTML, vai acima do elemento `<body>`

O `<head>` contém os _metadados_ para uma página da web. Metadados são informações sobre a página que não são exibidas diretamente na página da web. Diferentemente das informações dentro da tag `<body>` os metadados no cabeçalho são informações sobre a própria página. Vamos ver um exemplo.

Ele contém informações como [title](https://developer.mozilla.org/en-US/docs/Glossary/title) , links para `[<css>](<https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/css>)` \(se você deseja modelar seu conteúdo HTML com CSS\), links para favicons personalizados e outros

```markup
<! DOCTYPE html> 
<html lang="pt-br">> 
  <head>
     <meta charset="utf-8">
     <meta name="viewport" content="width=device-width, initial-scale=1">
     <link rel="stylesheet" type="text/css" href="style.css" />
     <title>Meu Site</title>
  </head>
  <body>
    <!-- Conteúdo do site, aparece dentro da tag body-->
  </body>
</html>

```

‌

`<meta charset="utf-8">` especifica a codificação de caracteres do documento — o conjunto de caracteres que o documento está autorizado a usar. `utf-8` é um conjunto de caracteres universal que inclui praticamente qualquer caractere de qualquer linguagem humana.

‌

### **Meta Tag para redes sociais.**

Quando você compartilha algum site nas redes sociais, você percebeu que quando coloca o link no post, visualiza uma imagem acompanhada de informações referente a página, imagens e título.‌

_Open Graph_ Markup é um protocolo que permite administrar e monitorar os dados que são construídos nas visualizações estruturação das páginas web.

permite que qualquer página da Web se torne um objeto rico em um gráfico social, saiba que não se trata apenas de embelezar seu post, mas, mas se pesquisarem sobre _marketing digital_, isso aumenta o tráfego da sua página, mas... sou desenvolvedor, preciso entender de marketing? não, mas acredito que quando você for desenvolver o seu site, você, vai querer que muitas pessoas visitem, conheça mais sobre você e possa surgir alguma oportunidade de trabalho, certo? então usando o _Open Graph_ Markup no seu código, vai te ajudar a atrair mais visitantes.

‌

### Como Implementar Open Graph no HTML

você colocará `<meta>`tags adicionais na `<head>`sua página da web. As quatro propriedades necessárias para cada página são:

```markup
<!--Exemplo-->
<head>
<title>Rede Cidadã</title>
<meta property="og:locale" content="pt_BR">
<meta property="og:title" content="Rede Cidadã - Vida e trabalho, um só valor">
<meta property="og:type" content="website">
<meta property="og:description" content="Somos uma organização com programas e projetos sociais em 11 Estados do Brasil, com atuação nas áreas de empregabilidade, aprendizagem, empreendedorismo e voluntariado.">
<meta property="og:url" content="<http://www.redecidada.org.br/>">
<meta property="og:image" content="http://../images/logo.jpg" />
...
</head>
...
</html>

```

![https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz\_%2F-M7yBvRp764w90Ao63y8%2F-M7yCUGELjfiZG-p8FJ-%2FCaptura de Tela 2020-05-22 a&#x300;s 18.06.21.png?alt=media&amp;token=f6f48e1a-4d7d-4ae4-8131-f899433440ec](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7yBvRp764w90Ao63y8%2F-M7yCUGELjfiZG-p8FJ-%2FCaptura%20de%20Tela%202020-05-22%20a%CC%80s%2018.06.21.png?alt=media&token=f6f48e1a-4d7d-4ae4-8131-f899433440ec)

Resultado do open graph, num post do facebook.Enter a caption for this image \(optional\)

### Caminho de arquivo

Caminhos de URL em HTML pode ser caminhos absolutos, como um URL completo, por exemplo: `https://developer.mozilla.org/en-US/docs/Learn`ou um caminho de arquivo relativo que links para um arquivo local na mesma pasta ou no mesmo servidor, por exemplo: `./style.css`. Os caminhos de arquivos relativos começam com `./`seguidos por um caminho para o arquivo local. `./`diz ao navegador para procurar o caminho do arquivo na pasta atual.

```markup
<!--Exemplo-->
pasta-projeto / 
| —— about.html 
| —— contact.html 
| —— index.html

```

```markup
<a href="<https://developer.mozilla.org/en-US/docs/Web>">a URL para este elemento âncora é um caminho de arquivo absoluto, link externo.</a> 
<a href="./about.html"> A URL para este elemento âncora é um caminho de arquivo relativo.</a>

```

Agora você conhece todos os elementos e configurações básicos necessários para estruturar uma página HTML e adicionar diferentes tipos de conteúdo.

Embora algumas tags tenham uma finalidade muito específica, como tags de imagem e vídeo, a maioria delas é usada para descrever o conteúdo que elas envolvem, o que nos ajuda a modificar e estilizar nosso conteúdo posteriormente. Aparentemente, há um número infinito de tags para usar \(muito mais do que ensinamos\). Saber quando usar cada um é baseado em como você deseja descrever o conteúdo do seu HTML. Tags descritivas e bem escolhidas são uma chave para o desenvolvimento da web de alta qualidade. Uma lista completa de tags HTML disponíveis pode ser encontrada [na documentação do Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) .

**Versões do HTML** O html na sua trajetória sofreu algumas mudanças com o objetivo de enriquecer a linguagem. a versão mais utilizada hoje no mercado é o HTML5 e, o principal mantenedor é a [WHATWG](https://whatwg.org/) é \*\( uma comunidade que padroniza e faz a documentação , foi fundada por desenvolvedores da Opera, Apple e Mozila, fazendo uma versão mais flexível do HTML que é o HTML5, \)\***HTML+ HTML 2.0 HTML 3.0 XHTML HTML 5.0**‌

O HTML5 é uma versão mais enxuta e com mais recursos, para maiores informações indicamos sempre acessar o site do WHATWG.

**Browser Core**

Hoje em dia podemos acessar um site de diversos ambientes seja em diferentes tipos de dispositivos e de sistema operacional, a web ela tem que ser única, portanto para que possamos ter acesso a um site de uma forma padronizada, o principal componente que precisamos para renderizar o HTML é o navegador.

**Principais Navegadores**

* Google Chrome
* Mozilla Firefox
* Edge
* Opera

**Motores de renderização dos Navegadores:**

A função do motor de renderização é renderizar, ou seja exibir os conteúdos solicitados na tela do navegador. Cada navegador utiliza um motor de renderização diferente as a especificações de cada linguagem de programação, são muito detalhadas e cada motor oferece uma única interpretação dessa especificação. Ex: propriedades css como: espaçamento, margen_s_, tamanho podem apresentar um pouco diferente em cada navegador.

* **WebKit -** Safari/Chrome
* **Gecko -** Firefox
* **Trident -** Internet Explorer
* **Presto -** Opera

_Obs: por esse motivo, quando estamos desenvolvendo um site em HTML, criamos um arquivo onde padronizamos todos essa propriedades CSS. \( ex: reset.css\)_

## **HTML5**

HTML5 é a mais recente evolução do padrão que define o [HTML](https://developer.mozilla.org/pt-BR/docs/HTML). **A semântica das novas marcações do HTML5**

Ao criar páginas da web, usamos uma combinação de HTML não semântico e _HTML semântico_ . A palavra semântica significa "relacionada ao significado", para que os elementos semânticos forneçam informações sobre o conteúdo entre as tags de abertura e fechamento.

_Um elemento semântico descreve claramente seu significado para o navegador e o desenvolvedor._

Exemplos de elementos **não-semânticos** : `<div>`e `<span>`- Não conta nada sobre o seu conteúdo.

Exemplos de **semânticas** elementos: `<form>`, `<table>`e `<article>`- Claramente define seu conteúdo.

Nas páginas web, temos que marcar qual tipo de conteúdo será colocado, como um _**cabeçalho, rodapé ou menu de navegação.**_

Nas versões anteriores do HTML não haviam tags com uma semântica apropriada para cada uma dessas divisões. Dessa forma, os desenvolvedores acabavam usando a tag &lt;div&gt; para todas as situações, e criando seus próprios padrões de nomenclatura através dos atributos **id** ou **class**.

{% hint style="info" %}
Para entender melhor isso, você pode comparar o HTML não-semântico com o de entrar em uma loja sem sinais nos corredores. Como os corredores não são rotulados, você não sabe quais são os produtos nesses corredores. No entanto, as lojas que possuem sinais para cada corredor tornam muito mais fácil encontrar os itens necessários, assim como o HTML Semântico.
{% endhint %}

No HTML5 foram criadas diversas tags semânticas para indicar aos user-agents quais conteúdos estão sendo inseridos em cada uma das divisão da página, organizando e padronizando o desenvolvimento.

![https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz\_%2F-M7xmiGiZh15Wi00EJp-%2F-M7xmxzzQVu4zYOc\_u6F%2FCaptura de Tela 2020-04-22 a&#x300;s 09.01.49.png?alt=media&amp;token=08a5f4c5-8586-4c35-af05-b22c2f47a701](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7xmiGiZh15Wi00EJp-%2F-M7xmxzzQVu4zYOc_u6F%2FCaptura%20de%20Tela%202020-04-22%20a%CC%80s%2009.01.49.png?alt=media&token=08a5f4c5-8586-4c35-af05-b22c2f47a701)

```markup
<!--Exemplo Estrutura básica HTML5-->
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Titulo do meu site</title>
</head>
<body>
<header>
    <img class="main-header-logo" src="" alt="">
</header>
   <article>
      <section>
         <h3>Titulo</h3>
         <p>Contúdo do Site</p>
      </section>
   <footer>
      <p>Footer</p>
   </footer>
</body>
</html>

```

**Vamos entender a diferença entre essas TAGs.**

**&lt;header&gt;** O novo elemento do HTML5 é usado para definir o cabeçalho de uma página ou seção, e pode conter logo, títulos, menu de navegação, campo de busca, etc.

**&lt;section&gt;** Como o próprio nome diz, ele pode conter qualquer tipo de conteúdo. Em um sentido mais amplo do termo, este elemento é uma versão mais semântica de uma div \(que significa “divisão”\). Outro uso comum deste elemento está relacionado a estrutura do conteúdo. O objetivo desse elemento é marcar uma seção da página. Seção pode ser um grupo de conteúdo de um assunto específico.

Ela foi desenvolvida para representar seções de um documento, essa é a idéia principal, ex: capítulos, títulos ou qualquer outra área do documento com o mesmo tema.

**&lt;article&gt;** Ao contrário de seção, artigo é um componente mais específico. Sua finalidade é envolver os principais conteúdos do seu documento em seções lógicas. Entradas de blog, artigos, o conteúdo da página podem ser incluídos dentro deste elemento. Combinado com o elemento SECTION, que completa a estrutura geral de um documento HTML5.

**&lt;aside&gt;** É usado para marcar informações adicionais que podem aprimorar outro elemento, mas não são necessárias para entender o conteúdo principal. Este elemento pode ser usado junto com outros elementos, como `<article>`ou `<section>`. Alguns usos comuns do `<aside>`elemento são para:

* Bibliografias
* Notas finais
* Comentários
* Enquetes
* Barras laterais editoriais
* Informação adicional

Podemos comparar o uso dela com a página de um jornal, teríamos uma página, com diversas seções.

```markup
<article id="esportes">
   <hgroup>
    <h1>Esportes no Brasil</h1>
    <h2>Um pouco sobre o que está acontecendo no mundo dos esportes</h2>
   </hgroup>
   <section id="futebol">
    <h1>Futebol</h1>
    <p>conteúdo</p>
   </section>
   <section id="basquete">
    <h1>Basquete</h1>
    <p>conteúdo</p>
   </section>
</article>

```

[_**Mais info sobre web semântica**_](https://pt.stackoverflow.com/questions/148753/como-usar-as-tais-tags-sem%c3%a2nticas)

{% hint style="info" %}
É importante observar que um _****_elemento`<section>` também pode ser colocado dentro do elemento `<article>`dependendo do contexto.
{% endhint %}

### Produtividade no Desenvolvimento

O Emmet é um kit de ferramentas para desenvolvedores da Web que pode melhorar bastante o seu fluxo de trabalho HTML e CSS:

![https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz\_%2F-M7xqvysh8XrZUYeJmOs%2F-M7xs3KGstWTsQN2O\_-M%2Femmet-multi-cursor.gif?alt=media&amp;token=36b29d41-43e5-4bb8-afa3-bf3992f63625](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M7xqvysh8XrZUYeJmOs%2F-M7xs3KGstWTsQN2O_-M%2Femmet-multi-cursor.gif?alt=media&token=36b29d41-43e5-4bb8-afa3-bf3992f63625)

Enter a caption for this image \(optional\)

[Guia do Emmet](https://docs.emmet.io/cheat-sheet/), agora é aprender para os trechos de código para agilizar o desenvolvimento do seus sites, vamos praticar.

## Introdução às Tabelas

Existem muitos sites na Internet que exibem informações como preços de ações, resultados esportivos, dados de faturas e muito mais. Esses dados são naturalmente de natureza tabular, o que significa que uma tabela geralmente é a melhor maneira de apresentar os dados.

Nesta parte do curso, aprenderemos como usar o `<table>`elemento HTML para apresentar informações em uma tabela bidimensional para os usuários. Vamos ver um exemplo no código abaixo:

```markup
<table>
    <tr> <!-- table row 1-->
      <th>Aluno</th><!--Coluna - table heading-->
      <th>Disciplina</th><!--Coluna - table heading-->
      <th>Nota</th><!--Coluna - table heading-->
    </tr>
    <tr><!-- Row 1 -->
      <td>Aluno 1</td><!--conteúdo - table data-->
      <td>Lógica</td><!--conteúdo - table data-->
      <td>8.0</td><!--conteúdo  - table data-->
    </tr>
    <tr><!-- Row 2 -->
      <td>Aluno 2</td><!--conteúdo - table data-->
      <td>HTML</td><!--conteúdo - table data-->
      <td>10</td><!--conteúdo - table data-->
    </tr>
</table>

```

[Untitled](https://www.notion.so/721a486a8dca4d8b81c5062aba6677b2)

## Introdução aos formulários HTML

Formulários fazem parte da vida cotidiana. Quando usamos um formulário, escrevemos informações e as entregamos a alguém para processar. Pense nas vezes em que você precisou preencher informações para vários aplicativos, como um emprego, uma conta bancária ou entregou um cartão de sugestão preenchido.

O elemento `<form>` é responsável por coletar informações para enviar para outro lugar. Toda vez que navegamos na Internet, entramos em contato com muitas formas e podemos nem perceber. Há uma boa chance de que, se você estiver digitando em um campo de texto ou fornecendo uma entrada, o campo em que você está digitando faz parte de um `<form>`

Nesta aula , examinaremos a estrutura e a sintaxe de um `<form>`e dos elementos que o preenchem.

## Como um formulário funciona

Podemos pensar na internet como uma rede de computadores que enviam e recebem informações. Os computadores precisam de uma _solicitação HTTP_ para saber como se comunicar. A solicitação HTTP instrui o computador receptor como lidar com as informações recebidas. Mais informações podem ser encontradas nesse artigo sobre [solicitações HTTP](https://www.codecademy.com/articles/http-requests) .

O elemento `<form>` é uma tag para coletar informações, mas precisamos enviar essas informações para outro lugar para processamento. Precisamos fornecer ao elemento `<form>` a localização de onde as informações vão e qual solicitação HTTP a ser feita. Dê uma olhada na exemplo abaixo:

```markup
<form action="/example.html"  method="POST"></form> 

```

No exemplo acima, criamos o esqueleto para um `<form>`que enviará informações para **example.html** como uma solicitação POST:

* O atributo `action` determina para onde as informações são enviadas.
* O atributo `method` Define qual método HTTP usar quando enviar um formulário. Pode ser GET\(padrão\) ou POST.

```markup
<form action="/example.html"  method="POST"> 
  <h1>Criando um formulário</h1> 
  <p>Vamos aprender a criar um formulário HTML.</p> 
</form>

```

### Formulário - Principais elementos/tipos

* O objetivo do `<form>`é permitir que os usuários insiram e enviem informações.
* O atributo `action`determina para onde vão as informações do formulário.
* O atributo `method`determina como as informações são enviadas e processadas.
* Para adicionar campos aos usuários para inserir informações, usamos o `<input>`elemento e configuramos o `type`atributo para um campo de nossa escolha:
  * A configuração `type`para `"text"`cria um campo de linha única para entrada de texto.
  * Definir `type`para `"password"`cria um campo de linha única que censura a entrada de texto.
  * A configuração `type`para `"number"`cria um campo de linha única para entrada de número.
  * Definir `type`para `"range"`cria um controle deslizante para selecionar em um intervalo de números.
  * Definir `type`para `"checkbox"`cria uma única caixa de seleção que pode ser emparelhada com outras caixas de seleção.
  * A configuração `type`para `"radio"`cria um botão de opção que pode ser emparelhado com outros botões de opção.
  * Definir `type`para `"list"`emparelhará o `<input>`com um `<datalist>`elemento se os `id`dois forem iguais.
  * A configuração `type`para `"submit"`cria um botão de envio.
* Um `<select>`elemento é preenchido com `<option>`elementos e renderiza uma seleção da lista suspensa.
* Um `<datalist>`elemento é preenchido com `<option>`elementos e trabalha com um `<input>`para pesquisar opções.
* Um `<textarea>`elemento é um campo de entrada de texto que possui uma área personalizável.
* Quando a `<form>`é enviado, os `name`campos que aceitam entrada e `value`os campos são enviados como `name=value`pares.

### Exemplo de um form.

```markup
<!DOCTYPE html>
<html>
<body>
<h2>Formulário HTML</h2>
<form action="/example.html">
  <label for="fname">Nome:</label><br>
  <input type="text" name="fname" value="nome"><br>
  <label for="lname">Sobrenome:</label><br>
  <input type="text" name="lname" value="sobrenome"><br><br>
  <input type="submit" value="Submit">
</form> 
</body>
</html>

```

![https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz\_%2F-M83dINaRnAx-zTQkVMQ%2F-M83eW3h8zXDuJ9vsShK%2FCaptura de Tela 2020-05-23 a&#x300;s 23.59.22.png?alt=media&amp;token=860171fd-c24c-495a-8307-103d7bfef786](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M83dINaRnAx-zTQkVMQ%2F-M83eW3h8zXDuJ9vsShK%2FCaptura%20de%20Tela%202020-05-23%20a%CC%80s%2023.59.22.png?alt=media&token=860171fd-c24c-495a-8307-103d7bfef786)

Enter a caption for this image \(optional\)

O primeiro valor para o atributo `type` que vamos falar é o `"text"`. Quando criamos o elemento `<input type="text">` , o navegador renderiza um campo de texto que os usuários podem digitar. Também é importante incluir o atributo `name` no `<input>` sem o `name`, as informações no `<input>`não serão enviadas quando enviar o `<form>`

‌

## Enviando o formulário

Lembre-se de que o objetivo de um formulário é coletar informações que serão enviadas. Essa é a função do botão enviar - os usuários clicam nele quando terminam de preencher as informações `<form>`e estão prontos para enviá-las. Agora que falamos sobre como criar vários elementos de entrada, vamos agora sobre como criar um botão de envio!

Observe o `value`atribuído ao `<input>`aparece como texto no botão enviar. Se não houver um `value`atributo, o texto padrão será exibido `Submit`no botão.

O uso do `<form>`elemento em conjunto com os outros elementos listados acima nos permite criar sites que levam em consideração os desejos e necessidades de nossos usuários. Aproveite a oportunidade para pegar o que aprendeu e aplicá-lo!

### Validando um Formulário

![https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz\_%2F-M83ff38Aty8p5b9lfiN%2F-M83fzZ8EsTymqCD33sQ%2Fform%2Bvalidation.gif?alt=media&amp;token=1082bdb9-9495-4215-93a2-c0148b74082f](https://gblobscdn.gitbook.com/assets%2F-M7-2eRyD9xvpTaq4bz_%2F-M83ff38Aty8p5b9lfiN%2F-M83fzZ8EsTymqCD33sQ%2Fform%2Bvalidation.gif?alt=media&token=1082bdb9-9495-4215-93a2-c0148b74082f)

Enter a caption for this image \(optional\)

A Validação é o conceito de verificar os dados fornecidos pelo usuário em relação aos dados necessários. O que vamos no HTML é _a validação do lado do cliente_ para verificar os dados no navegador \(o cliente\). Esta validação ocorre antes dos dados serem enviados para o servidor.

Permite dar feedback rapidamente aos usuários para campos específicos, em vez de solicitá-los a preencher um formulário novamente se os dados inseridos no formulário foram rejeitados.

required - nao permite deixar um campo em branco

valores mínimos e máximos aceitáveis ​​em um campo numérico.

* O `min`atributo para`"1"`
* O `max`atributo para`"10"`

Para definir um valor mínimo aceitável, usamos o `min`atributo e atribuímos um valor. Por outro lado, para definir um valor máximo aceitável, atribuímos ao `max`atributo um valor. Vamos ver isso no código:

Para definir um número mínimo de caracteres para um campo de texto, adicionamos o `minlength`atributo e um valor para definir um valor mínimo. Da mesma forma, para definir o número máximo de caracteres para um campo de texto, usamos o `maxlength`atributo e definimos um valor máximo

`minlength="5" maxlength="250"`

‌

## Combinando um padrão

Além de verificar o tamanho de um texto, também podemos adicionar uma validação para verificar como o texto foi fornecido. Nos casos em que queremos que a entrada do usuário siga diretrizes específicas, usamos o `pattern`atributo e atribuímos a ele uma _expressão regular_ ou regex. Expressões regulares são uma sequência de caracteres que compõem um padrão de pesquisa. Se a entrada corresponder ao regex, o formulário poderá ser enviado.

Digamos que desejássemos verificar um número de cartão de crédito válido \(um número de 14 a 16 dígitos\). Poderíamos usar o regex: `[0-9]{14,16}`que verifica se o usuário forneceu apenas números e se digitou pelo menos 14 dígitos e no máximo 16 dígitos.

Para adicionar isso a um formulário

```markup
<form action="/example.html" method="POST">
  <label for="payment">Cartao de crédito (no spaces):</label>
  <br>
  <input id="payment" name="payment" type="text" required pattern="[0-9]{14,16}">
  <input type="submit" value="Submit">
</form>

```

Com o `pattern`local, os usuários não podem enviar o `<form>`número com que não segue a regex. Quando tentarem, verão uma mensagem de validação da seguinte forma:

* As validações do lado do cliente acontecem no navegador antes que as informações sejam enviadas para um servidor.
* A adição do `required`atributo a um elemento relacionado à entrada validará que o campo de entrada possui informações.
* A atribuição de um valor ao `min`atributo de um elemento de entrada numérico validará um valor mínimo aceitável.
* A atribuição de um valor ao `max`atributo de um elemento de entrada numérico validará um valor máximo aceitável.
* A atribuição de um valor ao `minlength`atributo de um elemento de entrada de texto validará um número mínimo aceitável de caracteres.
* A atribuição de um valor ao `maxlength`atributo de um elemento de entrada de texto validará um número máximo aceitável de caracteres.
* Designar uma regex para `pattern`corresponder a entrada à regex fornecida.
* Se as validações em um `<form>`não passarem, o usuário receberá uma mensagem explicando o porquê e o `<form>`não poderá ser enviado.

Essas verificações rápidas ajudam a garantir que os dados de entrada estejam corretos e seguros para nossos servidores. Ele também ajuda a fornecer aos usuários um feedback imediato sobre o que eles precisam corrigir, em vez de esperar que um servidor envie essas informações.

‌

### Referências

* [https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
* [https://www.w3schools.com/html/html\_attributes.asp](https://www.w3schools.com/html/html_attributes.asp)
* [https://www.codecademy.com/learn/learn-html](https://www.codecademy.com/learn/learn-html)
* [https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
* [https://developer.mozilla.org/pt-BR/docs/Aprender/HTML/Introducao\_ao\_HTML/The\_head\_metadata\_in\_HTML](https://developer.mozilla.org/pt-BR/docs/Aprender/HTML/Introducao_ao_HTML/The_head_metadata_in_HTML)
* [https://ogp.me/](https://ogp.me/)
* [https://rockcontent.com/blog/meta-tags-para-redes-sociais/](https://rockcontent.com/blog/meta-tags-para-redes-sociais/)
* [https://developers.facebook.com/docs/sharing/web](https://developers.facebook.com/docs/sharing/web)
* [https://www.codecademy.com/learn/learn-html/modules/learn-html-forms/cheatsheet](https://www.codecademy.com/learn/learn-html/modules/learn-html-forms/cheatsheet)

### 

