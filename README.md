# pedido
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pedido Especial</title>

<style>
body{
    margin:0;
    font-family:Arial, sans-serif;
    text-align:center;
    background:linear-gradient(135deg,#ffe6f0,#fff);
    overflow:hidden;
}

.container{
    margin-top:30px;
    padding:20px;
}

img{
    width:320px;
    max-width:90%;
    border-radius:20px;
    box-shadow:0 8px 20px rgba(0,0,0,0.2);
}

h1{
    color:#d63384;
    margin-top:20px;
    padding:10px;
}

button{
    font-size:22px;
    padding:12px 24px;
    margin:15px;
    border:none;
    border-radius:12px;
    cursor:pointer;
    transition:0.2s;
}

#sim{
    background:#7dff9b;
}

#sim:hover{
    transform:scale(1.08);
}

#nao{
    background:#ff8a8a;
    position:absolute;
}
</style>
</head>

<body>

<div class="container">

    <!-- TROQUE foto.jpg pelo nome real da sua imagem no GitHub -->
    <img src="foto.jpg" alt="Nossa Foto">

    <h1>💖 Posso ir pra sua casa depois da reunião? 🥰</h1>

    <button id="sim" onclick="aceitou()">😍 Sim</button>
    <button id="nao" onclick="fugir()">😒 Não</button>

</div>

<script>
let tentativas = 0;

function aceitou(){
    alert("💘 Que bom sua gostosa. Fico feliz em ter aceitado me ver hj. Parabéns por usar seu livre arbítrio! Te amo muito ❤️");
}

function fugir(){
    tentativas++;

    let botao = document.getElementById("nao");

    if(tentativas >= 2){
        botao.style.display = "none";
        return;
    }

    let largura = window.innerWidth - 120;
    let altura = window.innerHeight - 60;

    let x = Math.random() * largura;
    let y = Math.random() * altura;

    botao.style.left = x + "px";
    botao.style.top = y + "px";
}

document.getElementById("nao").addEventListener("mouseover", fugir);
</script>

</body>
</html>
