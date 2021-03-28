# MDN HTML

## Anatomia de um elemento HTML
    <p>Meu gato é muito lindo</p>
    Tag de inicio / conteúdo / tag de fechamento
## Aninhando Elementos
Um elemento pode outros elementos internos, esse agrupamento é chamado de aninhamento
de elementos.
## Elementos em bloco versus elementos inline
Os elementos em bloco se agrupam um encima do outro, já os inline, se agrupam na 
mesma linha um com o outro.
## Elementos Vazios
Nem todas as tags precisam de uma tag de fechamento, esses que não precisam são
chamados de elementos vazios, no final eles tem um / para informa que está se fechando.
    <img src="url" />
## Atributos
As tags elementos podem ter atributos com características próprias
    <p class="class é o atributo"> 

## Atributos Booleanos
Esses atributos são aqueles que podem ser editáveis ou não.
    <input type="text" disabled="disabled">
## Elementos especiais no HTML
Para utilizar esses elementos especiais deve-se utilizar da notação &-comercial
    < -> &lt; 
    > -> &gt;
    " -> &quot;
    ' -> &apos;
    & -> &amp;
## Comentários
    <!-- O comentário vem aqui dentro -->

# HEAD 
O trabalho do cabeçalho é conter metadados, dados sobre o html específico, esses 
dados não são exibidos na tela mas é essencial para a configuração da pag.
## Adicionando um título
Para adicionar um title no head basta colocar o título entre a tag <title>
A tag <title> também é utilizada para dar o nome aos favoritos, quando o 
usuário define essa página como favorito. Também aparecem nos buscadores

## Metadados: o elemento <meta>
Definir a codificação de caracteres <meta charset="utf-8">
É uma boa prática utilizar dessa configuração, pois assim o seu site pode ser
lido em qualquer idioma humano, pois a codificação utf-8 é a codificação
universal.
Muitos elementos meta possuem o atributo name e content
name -> Informa uqe tipo de metadados está sendo utilizado
content -> Informa o conteúdo desse metadado.
<meta name="author" content="Tiago Neves">
<meta name="description" content="Esse é um dos primeiros sites">
Essas formas de definir os metadados fazem parte das atividades de SEO, que 
tem como fundamentos a habilidade de tornar as páginas mais relevantes
para os buscadores.

## Outros tipos de metadados
É possível utilizar metadados criados por empresas, para que quando o seu site
for linkado nesses sistemas o próprio sistema pode renderizar o que você 
definiu no metadado do seu site.
Existe também o favicon, em que se define uma imagem .ico para poder utilizar
essa imagem no lado do titulo e também na parte de favoritos.
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">

## CSS e JavaScript
CSS -> Definido no head para poder carregar os estilos junto com as pags
JavaScript -> Recomenda-se colocar no final da pag, para que o html e css carregue antes de realizar alguma operação com JS.

# Fundamentos do texto em HTML
## O básico: Cabeçalhos e Parágrafos
<p> -> Parágrafos
<h1> -> Títulos e subtítulos
Necessário para os temos de SEO. Basicamente é necessário também para questão de
acessibilidade e também para uma fácil estilização do site.

## Por que precisamos de semântica?
Para estabelecer um padrão de leitura pelos browsers e também pelo SEO.
Além de considerar a acessibilidade do site.
No caso, é possível utilizar qualquer elemento e estilizar em CSS, mas esse 
elemento perde o sentido semântico e nem os SEO e os sistemas de leitura de 
tela para deficientes visuais irá entender o que aquele elemento é.

## Listas
<ul> -> Listas não ordenadas
<li> -> Cada item da lista
<ol> -> Lista ordenada
É possível aninhar listas, utilizando tipo de listas diferentes.

## Importância e Ênfase
<strong> -> Importância no conteúdo
<em> -> Ênfase para o que está sendo dito.
Não se deve mais utilizar <b> ou <i>, pois isso não trás nenhum função semântica
ao código html. Utilizado apenas para estilizar quando o CSS não era tão presente
assim. Portante deve-se escapar dessas tags de apresentação.
