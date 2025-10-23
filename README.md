<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ReciclaJá ♻️</title>
<style>
body {
background-color: #3BA7A5; /* Azul do fundo */
font-family: 'Poppins', sans-serif;
color: #fff;
text-align: center;
padding: 40px;
}
h1 {
font-size: 2.5em;
color: #145A32;
}
input {
width: 80%;
padding: 12px;
font-size: 1em;
border: none;
border-radius: 8px;
margin-top: 20px;
}
button {
padding: 10px 20px;
background-color: #1E8449;
color: white;
border: none;
border-radius: 8px;
font-size: 1em;
margin-top: 10px;
cursor: pointer;
}
.resultado {
margin-top: 30px;
background: rgba(255,255,255,0.2);
border-radius: 10px;
padding: 20px;
}
.lixeira {
font-weight: bold;
}
</style>
</head>
<body>

<h1>♻️ ReciclaJá</h1>
<p>Digite o tipo de lixo e descubra como descartar corretamente!</p>

<input type="text" id="lixoInput" placeholder="Ex: garrafa PET, pilha, casca de banana...">
<br>
<button onclick="analisarLixo()">Ver descarte</button>

<div class="resultado" id="resultado"></div>

<script>
function analisarLixo() {
const entrada = document.getElementById("lixoInput").value.toLowerCase();
const resultado = document.getElementById("resultado");

let resposta = "";

if (entrada.includes("plástico") || entrada.includes("pet") || entrada.includes("garrafa") || entrada.includes("pote") || entrada.includes("saco")) {
resposta = "♻️ **Reciclável!**<br>🗑️ Lixeira: <span class='lixeira' style='color:#ff0000;'>Vermelha</span><br>💡 Dica: Lave antes de descartar para evitar contaminação.";
}
else if (entrada.includes("papel") || entrada.includes("caixa") || entrada.includes("folha") || entrada.includes("caderno")) {
resposta = "♻️ **Reciclável!**<br>🗑️ Lixeira: <span class='lixeira' style='color:#0000ff;'>Azul</span><br>💡 Dica: Evite descartar papel sujo ou engordurado.";
}
else if (entrada.includes("vidro") || entrada.includes("garrafa de vidro") || entrada.includes("frasco") || entrada.includes("pote de vidro")) {
resposta = "♻️ **Reciclável!**<br>🗑️ Lixeira: <span class='lixeira' style='color:#008000;'>Verde</span><br>💡 Dica: Cuidado com vidros quebrados! Envolva em papel antes de descartar.";
}
else if (entrada.includes("metal") || entrada.includes("lata") || entrada.includes("alumínio")) {
resposta = "♻️ **Reciclável!**<br>🗑️ Lixeira: <span class='lixeira' style='color:#ffff00;'>Amarela</span><br>💡 Dica: Amassar latas ajuda a economizar espaço.";
}
else if (entrada.includes("pilha") || entrada.includes("bateria") || entrada.includes("eletrônico")) {
resposta = "⚠️ **Lixo especial!**<br>🗑️ Leve a um ponto de coleta específico.<br>💡 Dica: Nunca jogue no lixo comum — pode contaminar o solo.";
}
else if (entrada.includes("comida") || entrada.includes("resto") || entrada.includes("banana") || entrada.includes("casca") || entrada.includes("maçã")) {
resposta = "🌱 **Lixo orgânico.**<br>🗑️ Lixeira: <span class='lixeira' style='color:#8B4513;'>Marrom</span><br>💡 Dica: Pode virar adubo por compostagem.";
}
else {
resposta = "🤔 Não tenho certeza sobre esse item.<br>Tente descrever melhor ou verifique se é reciclável.";
}

resultado.innerHTML = resposta;
}
</script>

<p style="margin-top:40px; color:#145A32;">Descarte certo, futuro limpo! 🌎</p>

</body>
</html>
