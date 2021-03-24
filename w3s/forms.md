# FORMS HTML

São usados para que os usuários possam inputar dados no servidor
<form> -> Usado para englobar um formulário.

<input /> -> O mais usado no formulário, onde o usuário irá interagir
<input type="Algum Tipo" /> -> Existe vários tipos de inputs, os mais usados:
text -> Campo de texto
radio -> Botão de rádio, usado para selecionar um de muitos
checkbox -> Mostra um selecionador, pode selecionar muito de muitos
submit -> Usado para enviar o formulário, quando clicado gera a ação do forms
button -> Mostra um botão clicável

<label> -> São usados para navegadores que usam leitor de tela e também para
selecionar radio buttons ao clicar na palavra, resumindo, é um bom uso.

O atributo name é usado para que os dados possam ser reconhecidos quando forem
imputados, então o nome de cada input será considerado ao entregar os dados.

## Atributos do Formulário

action -> Informa para onde irão os dados após serem imputados
<form action="/action_page.php">

target -> Define como a resposta chegará ao usuário. Se será numa nova janela
na mesma janela, etc. O padrão é _self, na mesma pagina.
<form action="/action.php" target="framename">

method -> Define qual o método HTTP que está sendo usado no formulário, se será
get, post, put, delete.
<form action="/action.php" method="get">
Só use a função get para poder usar a url para poder pesquisar depois, caso contrário utilize o metodo post, pois é possível enviar mais dados ao servidor.

autocomplete -> Informa se o input pode receber dados que o usuário já digitou
antes em outros inputs, caso não queria, deixe off.
<form action="/action.php" autocomplete="off">

novalidate -> Informa que os dados do formulário não devem ser validados quando inputados.
<form action="/action.php" novalidate="novalidate">

    Attribute	Description
    accept-charset	Specifies the character encodings used for form submission
    action	Specifies where to send the form-data when a form is submitted
    autocomplete	Specifies whether a form should have autocomplete on or off
    enctype	Specifies how the form-data should be encoded when submitting it to the server (only for method="post")
    method	Specifies the HTTP method to use when sending form-data
    name	Specifies the name of the form
    novalidate	Specifies that the form should not be validated when submitted
    rel	Specifies the relationship between a linked resource and the current document
    target	Specifies where to display the response that is received after submitting the form
## Form Elements

Existe vários elementos para o forms, cada qual com uma função diferente

input -> O mais usado, pode ter diferentes formatos dependendo do tipo
<input type="text" id="fname" name="fname">

label -> Utilizado para ser a parte visual do usuário, também ajuda na parte de selecionar radio buttons e checkbox.
<label for="nameElement"> -> for -> informa de qual elemento o label pertence.

select -> Cria uma dropdown lista, com várias opções para selecionar.
<select id="cars" name="cars" size="2" multiple> -> size, mostra de dois em dois valores / multiple, é possível selecionar várias opções, basta securar ctrl.
    <option value="volvo">Volvo</option>
    <option value="saab">Saab</option>
    <option value="fiat" selected>Fiat</option> -> Por padrão define o fiat
    <option value="audi">Audi</option>
</select>

textarea -> Define um multi-line input campo.
<textarea name="message" rows="10" cols="30">
rows -> Informa a quantidade de linhas que pode ler
cols -> Informa o tamanho da caixa de texto
</textarea>

button -> Define um botão clicável
<button type="button" onclick="alert('Eae')">Click me </button>


fieldset -> Informa que esse grupo é um campo relacionado a dados no form. Encapsula o formulário em sessões.
legend -> Define um titulo para esse campo de input de dados
```html
<form action="/action_page.php">
  <fieldset>
    <legend>Personalia:</legend>
    <label for="fname">First name:</label><br>
    <input type="text" id="fname" name="fname" value="John"><br>
    <label for="lname">Last name:</label><br>
    <input type="text" id="lname" name="lname" value="Doe"><br><br>
    <input type="submit" value="Submit">
  </fieldset>
</form>
```

datalist -> Define uma lista de opções pre-definidas. Bom para setar regiões.
<form action="/action_page.php">
  <input list="browsers">
  <datalist id="browsers">
    <option value="Internet Explorer">
    <option value="Firefox">
    <option value="Chrome">
    <option value="Opera">
    <option value="Safari">
  </datalist>
</form>

output -> Mostra a saída de alguma operação.
<form action="/action_page.php"
  oninput="x.value=parseInt(a.value)+parseInt(b.value)">
  0
  <input type="range"  id="a" name="a" value="50">
  100 +
  <input type="number" id="b" name="b" value="50">
  =
  <output name="x" for="a b"></output>
  <br><br>
  <input type="submit">
</form>

    Tag	Description
    <form>	Defines an HTML form for user input
    <input>	Defines an input control
    <textarea>	Defines a multiline input control (text area)
    <label>	Defines a label for an <input> element
    <fieldset>	Groups related elements in a form
    <legend>	Defines a caption for a <fieldset> element
    <select>	Defines a drop-down list
    <optgroup>	Defines a group of related options in a drop-down list
    <option>	Defines an option in a drop-down list
    <button>	Defines a clickable button
    <datalist>	Specifies a list of pre-defined options for input controls
    <output>	Defines the result of a calculation

## Input types

Existe muitoss tipos de inputs, o legal seria conhecer cada um e saber um canto
onde encontrar eles mais rapidamente para consulta depois.

    Attribute	Description
    checked	Specifies that an input field should be pre-selected when the page loads (for type="checkbox" or type="radio")
    disabled	Specifies that an input field should be disabled
    max	Specifies the maximum value for an input field
    maxlength	Specifies the maximum number of character for an input field
    min	Specifies the minimum value for an input field
    pattern	Specifies a regular expression to check the input value against
    readonly	Specifies that an input field is read only (cannot be changed)
    required	Specifies that an input field is required (must be filled out)
    size	Specifies the width (in characters) of an input field
    step	Specifies the legal number intervals for an input field
    value	Specifies the default value for an input field
## Input Attributes

readonly -> Informa que o input será apenas para leitura, não podendo editar.

disabled -> Informa que o input não poderá ser clicado.

size -> Informa até onde o elemento pode ser visto dentro do input.

maxlength -> Informa o tamanho do elemento que pode ser inputado, muito importante
para que fique em ordem com o banco de dados da aplicação.

min e max -> Usado para definir os valors mínimos e máximos de inputs de números

multiple -> Informa que multiplos elementos podem ser selecionados.

pattern -> Utiliza de expressões regulares para validar um input.

placeholder -> Dá um exemplo prévio de como o input deve ser usado.

required -> Informa se aquele input é necessário para ativar o submit

step -> Define a quantidade de passos numéricos que um input pode ter.

autofocus -> Quando a página carregar o elemento que tiver esse atributo vai ser 
focado primeiro.

height e width -> Define a altura e largura, respectivamente.

list -> Define uma lista de acordo com um datalist prévio e referenciando com o id do datalist.

autocomplete -> Define se o input vai poder acessar o histórico de inputs do usuário, vem habilitado por padrão

