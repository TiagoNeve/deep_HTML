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