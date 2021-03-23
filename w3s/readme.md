# w3schools

## html Styles
É possível usar na declaração da tag, ativando a propriedade

```html
    <tag style="propriedade:value";>
```
Todo elemento html pode receber um estilo próprio e eles podem ser configurados
em um arquivo css externo, onde é o recomendado de se colocar.

## Text Formatting 

Formatação de textos dentro do html utilizando tags, como:
```html
<br> -> Linha
<b> -> Coloca um fonte escura no elemento
<strong> -> Importante
<i> -> Itálico
<em> -> Com ênfase
<mark> -> Faz uma marcação 
<small> -> Deixa o texto pequeno
<del> -> Risca o texto
<ins> -> Coloca um sumbliado no elemento
<sub> -> Coloca um valor na parte debaixo
<sup> -> Coloca um valor encima do elemnto 
```

## Cochetes e citações

Utilizado para gerar citações e cochetes
```html
<blockquote> -> Define uma seção para a citação.
<q> -> Cria umas aspas na área do texto.
<abbr> -> Declara abreviações e é possível colcoar o título enssa abreviação.
<address> -> Para informações de contato. Deve-se sempre utilizar essas declarações, considerando sempre a acessibilidade.
<cite> -> Define o titulo de alguma obra de arte.
<bdo> -> Define a forma de como as letras serão organizadas no html
```
## Comentários

Os comentários são usados para os desenvolvedores se comunicarem entre si
```html
<!-- Aqui fica um comentário -->
```
## Cores html e Css

Simplesmente utilizado a tag style, não é recomendado utilizar diretamente no html
o correto seria separar essas estilizações em um arquivo css.
```html
<elemento style=""> -> inline css
<style></style> -> Internal css
<link rel="stylesheet" href="styles.css"> -> External css
```
## Links

Utilizado para hiperlinkar algum texto no html
```html
<a href="url"></a> -> Utilizado para hiperlinkar
<a href="url" target=""> -> Target propriedade, utilizado para definir como o 
navegador vai se comportar quando o link for clicado.
_self -> Padrão, abre o link na própria página
_blank -> Abre o link num local novo
_parent -> Abre o link no quadro pai
_top -> Abre o link no corpo todo da janela
url -> Temos as urls absolutas: http:// ou https://
url -> Temos as urls relativas: index.asp ou /css/default.asp, basicamente essas
urls buscam arquivos dentro do diretório.
<a href="default.asp">
<img src="link" alt="texto alternativo">
</a> -> Usando uma imagem para hiperlinkar
<a href="mailto:email@email.com">send email</a> -> mailto: Utilizado para enviar
um email para quem clicar na frase send email
<a title="Aqui vem um título"> -> Título dos links
No css é possível modificar a cor dos link, quando eles estão normais, clicados
com o mouse por cima e quando estão clicados mas segurados.
<style>
a:hover {}
a:link {}
a:visited {}
a:active {}
</style>
É possível ciruclar por dentro da página utilizando os links, basta definir um 
id no elemento e hiperlinkar um texto com o href="#nomeDoId"
```
## Imagem
Utilizado para renderizar uma imagem no html, pode utilizar links absolutos
ou relativos na escolha da imagem.
```html
<img src="url" alt="Texto alternativo">
```
É possível estilizar o tamanho da imagem utilizando css.
Com as propriedades width e height.
É possível colocar gifs na tag img, para que possa ser renderizado uma imagem 
animada.
A imagem pode flutuar entre os elementos, utilizando a proprieade CSS float.
```html
<img src="url" alt="Alternative" style="float:right or left or top">
```
    APNG	Animated Portable Network Graphics	.apng
    GIF	Graphics Interchange Format	.gif
    ICO	Microsoft Icon	.ico, .cur
    JPEG	Joint Photographic Expert Group image	.jpg, .jpeg, .jfif, .pjpeg, .pjp
    PNG	Portable Network Graphics	.png
    SVG	Scalable Vector Graphics	.svg

Mapa de imagem, é possível clicar em determinada áreas da imagem e hiperlinkar
essas áreas para determinadas urls.
```html
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">

<map name="workmap">
    <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
</map>
```
Primeiro é necessário definir uma imagem e seu map, com o atributo *usemap*
Segundo, criar uma tag <map name="namemap"> com o atríbuto name para definir
o id do map.
Terceiro, definir as áreas clicáveis usando o elemento <area>, recebe alguns 
parâmetros como shape: 
* rect -> Uma área retangular
* circle -> Uma área circular
* poly -> Uma área poligonal
* default -> A área total da imagem

    RECT: É preciso definir as coordenadas da imagem que será clicada, para isso
    pega-se a coordenada superior esquerda e depois a inferior direita, dessa 
    forma a área vai pegar todo o conteúdo dessa região.

    CIRCLE: Primeiro é preciso definir a coordenada x, y do centro do circulo,
    depois basta definir o seu raio em pixels. (Mais fácil e.e)

    POLY: É preciso de muitos pontos de coordenadas para definir a área clicável
    de um poligono aleatório, sempre tente pegar o máximo de coordenadas possíveis.

É possível utilizar javascript para definir o que acontece quando o image map for
clicada, bastando utilizar a propriedade onclick=""

Existe a possibilidade de utilizar uma imagem de fundo em CSS.
utilizando as propriedades do background.
```CSS
body {
    background-image: url('img.apng');
    background-repeat: no-repeat;
    background-attachment: fixed; /* Irá permitir que o elemento seja todo coberto */
    background-size: cover; /* Irá cobrir todo o elemento */
}
```

O elemento <picture> posibilita mostra diferentes imagens em diferentes tipos
de dispositivos.
Por exemplo, em determinado agente que solicitar a requisição não poder rodar
determinada imagem, pode-se colocar outra no lugar dependo da forma que a 
condicional foi adicionada.
```html
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture>
```
O elemento picture é geralmente utilizado para o propósito de largura de banda,
Suporte de formato de imagem, alguns browsers não reconhece alguns formatos,
então utiliza alternativas de imagens em determinadas extensões.

## Tabelas

Utiliza o elemento <table>, depois define a primeira linha <tr> e as colunas dentro dessa linha <th> junto com os seus elementos.
```html
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
</style>
<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>
```
É possível espandir uma coluna utilizando a propriedade colspan="número de colunas"
<th colspan="2">
Assim como é possível espandir as linhas utilizando a propriedade:
rowspan="Número de linhas a espandir"
<th rowspan="2">
Existe a possíbilidade de atribuir um title a tabela, utilizando o elemento
<caption>, ele deve estar dentro da tag <table>

    Tag	Description
    <table>	Defines a table
    <th>	Defines a header cell in a table
    <tr>	Defines a row in a table
    <td>	Defines a cell in a table
    <caption>	Defines a table caption
    <colgroup>	Specifies a group of one or more columns in a table for formatting
    <col>	Specifies column properties for each column within a <colgroup> element
    <thead>	Groups the header content in a table
    <tbody>	Groups the body content in a table
    <tfoot>	Groups the footer content in a table

## Listas
Temos as listas desordenadas <ul> e as ordeanadas <ol>, além de as listas
descritivas <dl>
```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```
É possível ter lista por dentro de listas, basta declarar qual o tipo de lista
usando os elementos, <ul>, <ol>, <dl>

Uma peculiaridade das listas ordenadas é a possibilidade de definir qual o tipo
de ordenação que será utilizada, podendo ter letras, número ou algoritmos romanos.
utilizando a propriedade <ol type="A">
Outra peculiaridade é definir por qual núemro irá começar a ordenação, basta
definir a propriedade <ol start="100">