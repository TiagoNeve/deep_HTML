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