<!DOCTYPE html>
<html lang="PT-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Formulário</title>
    <link rel="stylesheet" href="Formes.css">
    <script src="Formes.js" defer></script>
</head>
<body>
    <div class="container">
    <div class="conteiner">
    <label for="nome"> Nome:</label>
    <input type="text" name="nome" id="nome">
    <button onclick="mostrarNome()" id="butãoUm"> Enviar</button>

    <p id="resposta"></p>

    <label for="altura">Digite a altura:</label>
    <input type="number" name="altura" id="altura">
    <label for="largura">Digite a largura:</label>
    <input type="number" name="largura" id="largura">
    <button onclick="calcularArea()" id="calcular"> x </button>
    <button onclick="mais()" id="mais"> + </button>
    <button onclick="menos()" id="menos"> -</button>
    <button onclick="dividir()" id="divisão"> ÷ </button>
    
    <p id="resultado"></p>
    <p id="resultado"></p>
    <p id="resultado"></p>
    <p id="resultado"></p>
    </div>
    </div>
    
</body>
</html>

var nome = document.getElementById("nome")
var resp = document.getElementById("resposta")

var altura = document.getElementById("altura")
var largura = document.getElementById("largura")

function mostrarNome () {
   resp.innerText = "olá, " + nome.value
}

function calcularArea () {
    let area = altura.value * largura.value
    document.getElementById("resultado").innerText = "Resultado é " + area
}

function mais () {
    let camelo = Number(altura.value) + Number(largura.value)
    document.getElementById("resultado").innerText = "Resultado é " + camelo
}

function menos () {
    let cavalo = Number(altura.value) - Number(largura.value)
    document.getElementById("resultado").innerText = "Resultado é " + cavalo
}

function dividir () {
    let burro = Number(altura.value) / Number(largura.value)
    document.getElementById("resultado").innerText = "Resultado é " + burro
}
