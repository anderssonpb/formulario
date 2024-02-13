Criar um formulário de pesquisa

Objetivo: Construa um aplicativo que seja funcionalmente igual a https://survey-form.freecodecamp.rocks. Não copie este projeto de demonstração.

Histórias de usuário:

    Você deve ter um título de página em um elemento h1 com o id title
    Você deve ter uma breve explicação em um elemento p com o id description
    Você deve ter um elemento form com o id survey-form
    Dentro do elemento do formulário, deve ser obrigatório inserir seu nome em um campo input que tenha um id name e um type text
    Dentro do elemento do formulário, deve ser obrigatório inserir seu e-mail em um campo input que tenha um id email
    Se for informado um e-mail que não esteja formatado corretamente, um erro de validação HTML5 deve ser mostrado
    Dentro do formulário, você pode inserir um número em um campo input que tenha o id number
    A entrada de número não deve aceitar algo que não seja números, impedindo que você os digite ou mostrando um erro de validação do HTML5 (dependendo do seu navegador).
    Se forem inseridos números fora do intervalo do campo de entrada do número, intervalo esse definido pelos atributos min e max, um erro de validação de HTML5 deve ser mostrado
    Para os campos de entrada (inputs) name, email e number dentro do formulário, deve haver elementos label correspondentes que descrevam o propósito de cada campo com os seguintes ids: id="name-label", id="email-label" e id="number-label"
    Para os campos de entrada name, email e number, deve haver um texto placeholder (texto ilustrativo) que forneça uma descrição ou instruções para cada campo
    Dentro do elemento do formulário, você deve ter um elemento de menu suspenso select com um id dropdown e pelo menos duas opções para escolher
    Dentro do elemento do formulário, você pode selecionar uma opção de um grupo de pelo menos dois botões de opção (radio) que serão agrupados usando o atributo name
    Dentro do elemento de formulário, deve ser possível selecionar vários campos de uma série de caixas de seleção (checkboxes). Cada um desses campos deve ter um atributo value
    Dentro do elemento de formulário, você receberá uma textarea para comentários adicionais
    Dentro do elemento de formulário, você receberá um botão com o id submit para enviar as informações

Atenda às histórias de usuário e passe em todos os testes abaixo para concluir este projeto. Dê ao projeto o seu próprio estilo pessoal. Boa programação!

Observação: não se esqueça de adicionar <link rel="stylesheet" href="styles.css"> em seu HTML para vincular sua folha de estilo e aplicar seu CSS



<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Formulário de Pesquisa</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1 id="title">Formulário de Pesquisa</h1>
  <p id="description">Preencha este formulário para nos ajudar a melhorar nossos serviços.</p>
  <form id="survey-form">
    <label for="name" id="name-label">Nome:</label>
    <input type="text" id="name" name="name" placeholder="Digite seu nome completo" required>
    <br>
    <label for="email" id="email-label">E-mail:</label>
    <input type="email" id="email" name="email" placeholder="Digite seu endereço de e-mail" required>
    <br>
    <label for="number" id="number-label">Número:</label>
    <input type="number" id="number" name="number" min="1" max="100" placeholder="Digite um número entre 1 e 100">
    <br>
    <label for="dropdown" id="dropdown-label">Selecione uma opção:</label>
    <select id="dropdown" name="dropdown">
      <option value="opção1">Opção 1</option>
      <option value="opção2">Opção 2</option>
      <option value="opção3">Opção 3</option>
    </select>
    <br>
    <p>Qual sua opinião sobre nosso serviço?</p>
    <input type="radio" id="opinião1" name="opinião" value="bom">
    <label for="opinião1">Bom</label>
    <br>
    <input type="radio" id="opinião2" name="opinião" value="regular">
    <label for="opinião2">Regular</label>
    <br>
    <input type="radio" id="opinião3" name="opinião" value="ruim">
    <label for="opinião3">Ruim</label>
    <br>
    <br>
    <p>Comentários adicionais:</p>
    <textarea id="comentarios" name="comentarios" rows="4" cols="50"></textarea>
    <br>
    <button type="submit" id="submit">Enviar</button>
  </form>
</body>
</html>

-----------------------------CSS-------------------------------------------------------------------


body {
  font-family: sans-serif;
  margin: 20px;
}

h1 {
  text-align: center;
  font-size: 24px;
}

p {
  margin-bottom: 15px;
}

form {
  border: 1px solid #ccc;
  padding: 20px;
  border-radius: 5px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input, select, textarea {
  width: 100%;
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 3px;
  margin-bottom: 10px;
}

input[type="radio"] {
  margin-right: 5px;
}

textarea {
  height: 100px;
}

#submit {
  background-color: #4CAF50;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

#submit:hover {
  background-color: #449A48;
}

