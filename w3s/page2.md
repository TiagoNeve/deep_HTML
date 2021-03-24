#  DEEP HTML

## Layout Elements e Tecnicas

Os elementos do layout, utilizando html semântico são:
<header>
<nav>
<section>|<aside>
<article>|
<footer>

Onde: header -> Define o cabeçalho da página
nav -> A navegação da página
section -> Define as seções da página
article -> Define o conteúdo da página
aside -> Define o conteúdo ao lado da página, como um link de pags a mais.
footer -> Define o rodapé da página
details -> Define conteúdo adicional que o usuário pode querer visualizar
summary -> Define um cabeçalho para o elemento details

Existe 4 tecnicas de layout:
* CSS framework -> Para criação de layouts rapidamente
* CSS float property -> Mais fácil de usar, posicionando os elementos.
* CSS flexbox -> Utilizado para controlar como a pag ficará em dispositivos diferentes
* CSS grid -> Sistema de grades, usando linhas e colunas para estruturar a pag.

## Responsive

Ter uma página responsiva significa ter uma página que pode se adaptar a tamanhos
diferentes de telas, o CSS vai automaticamente definir tamanhos, esconder 
elementos, mostrar novos botões, organizar conteúdos, tudo de acordo com o 
tamanho da tela.

    TABLETS: max-width:800px

    MOBILE: max-width:500px

Para criar páginas responsivas deve setar o viewport meta tag.
<meta name="viewport" content="width=device-width, initial-scale=1.0">

Se a imagem estiver com width=100%, essa imagem vai responder modificando nas 
laterais e embaixo. Para que a imagem não aumente muito de tamanho, deve-se 
setar a propriedade **max-width=100%**, assim a imagem vai ficar no seu tamanho
original. Se a tela ficar menor, a mesma será redimensionada.

    Como dito anteriormente é possível setar imagens diferentes para largura de
    telas diferentes, usando o elemento <picture>

Os textos podem receber uma responsividade utilizando a unidade *vw*, view width
```html
<h1 style="font-size:10vw">Eu sou responsivo</h1>
```
Dessa forma o texto vai aumentar ou diminuir de acordo com o tamanho da tela.


### Media Queries

Com media queries é possível modificar totalmente o layout de uma pag ao chegar
em determinado tamanho. Por exemplo, numa página tem um conteúdo que em telas
grandes mostra seus elementos horizontalmente, mas em telas pequenas usam.

```css
@media only screen and (max-width:500px) {
    
}
```
Frameworks de responsividade:
W3.CSS -> https://www.w3schools.com/w3css/4/w3.css
Bootstrap -> https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css

## Computer Code Elementos

<code> -> É possível colocar sintax no conteúdo.
<kbd> -> Atalhos do teclado vão fazer determinada função.
<samp> -> Mostra um output de tipo de programa de computador, sua font muda tbm
<pre> -> Mostra exatamente como o texto é gerado, com espaços extras e \n
<var> -> Define como variável e mostra em italic
