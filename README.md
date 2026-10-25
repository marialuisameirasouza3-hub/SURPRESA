
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Você de lá e eu de cá ❤️</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    min-height: 100vh;
    overflow-x: hidden;
    font-family: Georgia, "Times New Roman", serif;
    color: white;

    background:
        radial-gradient(circle at 15% 20%, #ffffff 0 1px, transparent 2px),
        radial-gradient(circle at 75% 15%, #ffffff 0 1px, transparent 2px),
        radial-gradient(circle at 35% 70%, #ffffff 0 1px, transparent 2px),
        radial-gradient(circle at 85% 75%, #ffffff 0 1px, transparent 2px),
        linear-gradient(135deg, #120b1c, #32172b, #71384f);

    background-size: 100px 100px, 130px 130px, 170px 170px, 200px 200px, cover;

    display: flex;
    justify-content: center;
    align-items: center;
    padding: 35px 15px;
}

/* LUA */

.lua {
    position: fixed;
    top: 35px;
    right: 45px;
    width: 80px;
    height: 80px;
    border-radius: 50%;
    background: #fff5df;
    box-shadow: 0 0 40px rgba(255, 238, 190, .55);
}

.lua::after {
    content: "";
    position: absolute;
    top: -8px;
    left: 20px;
    width: 80px;
    height: 80px;
    border-radius: 50%;
    background: #1a0e23;
}

/* ESTRELAS */

.estrela {
    position: fixed;
    color: white;
    animation: piscar 2.5s infinite alternate;
}

.e1 { top: 12%; left: 12%; }
.e2 { top: 25%; left: 80%; }
.e3 { top: 65%; left: 8%; }
.e4 { top: 78%; left: 85%; }
.e5 { top: 45%; left: 90%; }
.e6 { top: 82%; left: 55%; }

@keyframes piscar {
    from {
        opacity: .2;
        transform: scale(.7);
    }
    to {
        opacity: 1;
        transform: scale(1.3);
    }
}

/* CONTEÚDO */

.container {
    width: 100%;
    max-width: 680px;
    text-align: center;
    position: relative;
    z-index: 5;
}

.intro {
    animation: aparecer 1.5s ease;
}

.intro h1 {
    font-size: 34px;
    font-weight: normal;
    line-height: 1.3;
    margin-bottom: 18px;
}

.intro h1 span {
    color: #ffb8cc;
}

.intro p {
    font-size: 18px;
    line-height: 1.7;
    color: #f9eaf0;
}

.subtexto {
    margin-top: 10px;
    color: #ffc6d7 !important;
    font-style: italic;
}

/* FOTOS */

.fotos {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin: 28px 0;
}

.foto {
    width: 145px;
    height: 175px;
    padding: 7px;
    background: white;
    box-shadow: 0 12px 30px rgba(0,0,0,.4);
}

.foto:first-child {
    transform: rotate(-5deg);
}

.foto:last-child {
    transform: rotate(5deg);
}

.foto img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* CAIXA */

.caixa-area {
    margin-top: 30px;
}

.caixa {
    width: 245px;
    height: 185px;
    position: relative;
    margin: auto;
    cursor: pointer;
    transition: .4s;
}

.caixa:hover {
    transform: scale(1.06);
}

.corpo {
    position: absolute;
    bottom: 0;
    left: 10px;
    width: 225px;
    height: 125px;
    border-radius: 8px 8px 18px 18px;

    background: linear-gradient(135deg, #873951, #c66c88);

    box-shadow: 0 20px 40px rgba(0,0,0,.4);
}

.tampa {
    position: absolute;
    top: 25px;
    left: 0;
    width: 245px;
    height: 52px;
    border-radius: 8px;

    background: linear-gradient(135deg, #bd5e7c, #e18da7);

    z-index: 4;
    transform-origin: left center;
    transition: 1s ease;

    box-shadow: 0 8px 18px rgba(0,0,0,.3);
}

.fita-vertical {
    position: absolute;
    bottom: 0;
    left: 103px;
    width: 38px;
    height: 125px;
    background: #f4d0da;
    z-index: 2;
}

.fita-horizontal {
    position: absolute;
    top: 39px;
    left: 0;
    width: 245px;
    height: 25px;
    background: #f4d0da;
    z-index: 5;
}

.laco {
    position: absolute;
    top: -2px;
    left: 91px;
    font-size: 45px;
    z-index: 8;
    transition: .4s;
}

.instrucao {
    margin-top: 18px;
    color: #f8dce6;
    font-size: 15px;
    animation: pulsar 1.8s infinite;
}

/* MENSAGEM */

.mensagem {
    display: none;
    margin: 30px auto 0;

    max-width: 600px;

    padding: 32px 25px;

    border-radius: 25px;

    background: rgba(255,255,255,.10);
    border: 1px solid rgba(255,255,255,.25);

    backdrop-filter: blur(13px);

    box-shadow: 0 20px 60px rgba(0,0,0,.4);

    animation: subir .9s ease;
}

.mensagem h2 {
    color: #ffb8cc;
    font-size: 28px;
    font-weight: normal;
    margin-bottom: 22px;
}

.letra {
    white-space: pre-line;
    font-size: 17px;
    line-height: 2;
    color: #fff4f7;
    max-height: 430px;
    overflow-y: auto;
    padding: 5px 15px;
    text-align: center;
}

.coracao {
    font-size: 36px;
    margin: 20px 0;
    animation: bater 1.4s infinite;
}

button {
    border: none;
    padding: 11px 24px;
    border-radius: 30px;
    background: #d87996;
    color: white;
    font-family: Georgia, serif;
    cursor: pointer;
    transition: .3s;
}

button:hover {
    background: #b95776;
    transform: scale(1.05);
}

/* ABERTURA */

.aberto .tampa {
    transform: rotate(-28deg) translate(-20px, -55px);
}

.aberto .laco {
    opacity: 0;
}

.aberto .caixa {
    display: none;
}

.aberto .instrucao {
    display: none;
}

.aberto .mensagem {
    display: block;
}

/* ANIMAÇÕES */

@keyframes aparecer {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes subir {
    from {
        opacity: 0;
        transform: translateY(35px) scale(.96);
    }

    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }
}

@keyframes pulsar {
    50% {
        opacity: .5;
    }
}

@keyframes bater {
    50% {
        transform: scale(1.2);
    }
}

/* CELULAR */

@media (max-width: 600px) {

    .lua {
        width: 55px;
        height: 55px;
        right: 20px;
        top: 20px;
    }

    .lua::after {
        width: 55px;
        height: 55px;
    }

    .intro h1 {
        font-size: 27px;
    }

    .intro p {
        font-size: 16px;
    }

    .foto {
        width: 120px;
        height: 150px;
    }

    .mensagem {
        padding: 25px 15px;
    }

    .letra {
        font-size: 16px;
        line-height: 1.8;
    }
}

</style>
</head>

<body>

<div class="lua"></div>

<div class="estrela e1">✦</div>
<div class="estrela e2">✧</div>
<div class="estrela e3">✦</div>
<div class="estrela e4">✧</div>
<div class="estrela e5">✦</div>
<div class="estrela e6">✧</div>


<div class="container" id="pagina">

    <!-- TEXTO INICIAL -->

    <div class="intro">

        <h1>
            Há quase um  ano era
            <span>você de lá</span>
            e eu de cá... ❤️
        </h1>

        <p>
            Olhando o mesmo céu,<br>
            mesmo com toda essa distância.
        </p>

        <p class="subtexto">
            Uma pequena surpresa para você...
        </p>

   

   

    <!-- CAIXINHA -->

    <div class="caixa-area">

        <div class="caixa" onclick="abrirSurpresa()">

            <div class="tampa"></div>

            <div class="corpo">

                <div class="fita-vertical"></div>

            </div>

            <div class="fita-horizontal"></div>

            <div class="laco">🎀</div>

        </div>

        <div class="instrucao">
            ✨ Clique na caixinha para abrir ✨
        </div>

    </div>


    <!-- SURPRESA -->

    <div class="mensagem">

        <h2>
            Para você... ❤️
        </h2>

        <div class="letra">

            <!--
            
        
            -->

            Você de lá e eu de cá
Olhando o mesmo céu
Que distância cruel
Assisto o tempo passar
Tento me dispersar
Olhando o celular
Metade do meu coração
Só quer te ver de novo
E a outra só pensa em você
Não tem nenhum espaço
Pra eu amar alguém de novo
Em mim só existe você
E nessas horas
Meu sorriso é passageiro
É aí que eu percebo
A falta que me faz você
E nessas horas
Eu nem ligo pra dinheiro
Pra eu me sentir inteiro
Só preciso de você, de você
Oh
E você de lá e eu de cá
Olhando o mesmo céu
Que distância cruel
Eu assisto o tempo passar
Tento me dispersar
Olhando o celular
Metade do meu coração
Só quer te ver de novo
E a outra só pensa em você
Não tem nenhum espaço
Pra eu amar alguém de novo
Em mim só existe você
E nessas horas
Meu sorriso é passageiro
É aí que eu percebo
A falta que me faz você
E nessas horas
Que eu nem ligo pra dinheiro
Pra eu me sentir inteiro
Só preciso de você
E nessas horas
Meu sorriso é passageiro
E é aí que eu percebo
A falta que me faz você
E nessas horas
Que eu nem ligo pra dinheiro
Pra eu me sentir inteiro
Só preciso de você, de você
Oh
        </div>

        <div class="coracao">
            ❤️
        </div>

        <button onclick="fecharSurpresa()">
            Fechar a surpresa
        </button>

    </div>

</div>


<script>

function abrirSurpresa() {

    document
        .getElementById("pagina")
        .classList.add("aberto");

}

function fecharSurpresa() {

    document
        .getElementById("pagina")
        .classList.remove("aberto");

}

</script>

</body>
</html>
