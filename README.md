<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartas Românticas com Explosão de Corações</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            height: 100vh;
            margin: 0;
            overflow-y: scroll;
            background-color: #f0e6f7;
            scroll-behavior: smooth;
            position: relative;
        }

        /* Ocultar a barra de rolagem */
        body::-webkit-scrollbar {
            display: none;
        }

        body {
            scrollbar-width: none;
            -ms-overflow-style: none;
        }

        .background-gif {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('cat.gif') center center / cover no-repeat;
            z-index: -1;
            opacity: 0.7;
        }

        .container-cartas {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 100px;
            padding: 40px;
            z-index: 1;
        }

        .envelope {
            position: relative;
            width: 400px;
            height: 250px;
            background-color: #fddde6;
            border: 2px solid #d1a1b2;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            transition: all 0.5s ease-in-out;
            backdrop-filter: blur(5px);
        }

        .envelope::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            height: 120px;
            background-color: #ffd1dc;
            clip-path: polygon(0 0, 100% 0, 50% 100%);
            transition: transform 0.5s ease-in-out;
            transform-origin: top;
        }

        .conteudo {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #fddde6;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            box-sizing: border-box;
            text-align: center;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .conteudo p {
            font-family: 'Arial', sans-serif;
            font-size: 18px;
            color: #a03b4c;
            margin: 0;
        }

        .botao-abrir {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #f28b82;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 18px;
            transition: background-color 0.3s ease;
        }

        .botao-abrir:hover {
            background-color: #d06261;
        }

        .envelope.aberto::before {
            transform: rotateX(180deg);
        }

        .envelope.aberto .conteudo {
            opacity: 1;
        }

        /* Estilos para os corações */
        .heart {
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: red;
            transform: rotate(-45deg);
            animation: fall 2s ease-in-out forwards;
            opacity: 0;
        }

        .heart::before,
        .heart::after {
            content: '';
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: red;
            border-radius: 50%;
        }

        .heart::before {
            top: -15px;
            left: 0;
        }

        .heart::after {
            left: 15px;
            top: 0;
        }

        /* Animação de queda dos corações */
        @keyframes fall {
            0% {
                opacity: 1;
                transform: translateY(-50px) rotate(-45deg);
            }
            100% {
                opacity: 0;
                transform: translateY(100vh) rotate(-45deg);
            }
        }
    </style>
</head>
<body>

    <div class="background-gif"></div>

    <div class="container-cartas">
        <!-- Carta 1 -->
        <div class="envelope" id="envelope1">
            <div class="conteudo">
                <p><strong>Carta 1:</strong> ola totosa parece que fiz outra supresinha pra vc, problema é seu pra me suportar, ninguem mandou ser a garota do meu sonho.</p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope1')">Abrir Carta</button>

        <!-- Carta 2 -->
        <div class="envelope" id="envelope2">
            <div class="conteudo">
                <p><strong>Carta 2:</strong> to aqui morrendo de saudades sabia ?, hoje faz 94 dias mais de 3 meses desde a primeira vez do dia 06/agosto/2024 que eu vi a menina mais linda, bela, gostosa, fofa, doce, style e apaixonante da minha vida (estou apaixonado por essa garota) </p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope2')">Abrir Carta</button>

        <!-- Carta 3 -->
        <div class="envelope" id="envelope3">
            <div class="conteudo">
                <p><strong>Carta 3:</strong> sei que faz bastante tempo que a gente nao se ve, mas posso afirmar q só pensei em vc uma vez durante todos esses dia isso pq vc nao sai da minha mente. você é meu melhor pensamento.</p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope3')">Abrir Carta</button>

        <!-- Carta 4 -->
        <div class="envelope" id="envelope4">
            <div class="conteudo">
                <p><strong>Carta 4:</strong> quero q nao seja mais so na minha memoria e seja logo logo de vdd eu te enchendo a paciencia porem sabendo q posso te chamar de minha namorada </p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope4')">Abrir Carta</button>

        <!-- Carta 5 -->
        <div class="envelope" id="envelope5">
            <div class="conteudo">
                <p><strong>Carta 5:</strong> vc deve achar q sou um manezão emocionado e bla bla bla, mas se tem uma certeza q eu tenho, essa certeza é vc sami.</p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope5')">Abrir Carta</button>

        <!-- Carta 6 -->
        <div class="envelope" id="envelope6">
            <div class="conteudo">
                <p><strong>Carta 6:</strong> nao vou para de sempre fazer alguma coisinha pra você, mesmo que vc ache bobeira. </p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope6')">Abrir Carta</button>

        <!-- Carta 7 -->
        <div class="envelope" id="envelope7">
            <div class="conteudo">
                <p><strong>Carta 7:</strong> nao sei se vc nao gosta ou so tem vergoinha, vc nao fala muito essas coisinha meio sentimentais.</p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope7')">Abrir Carta</button>

        <!-- Carta 8 -->
        <div class="envelope" id="envelope8">
            <div class="conteudo">
                <p><strong>Carta 8:</strong> eeee provavelmente deve ta rindo, sorrindo, sorrendo, sorraiando, sorrizando, carai nao sei como fala kekekkekekekekekek mas to sentindo sua falta mesmo q fosse pra te ver so por uns minutinhos  </p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope8')">Abrir Carta</button>

        <!-- Carta 9 -->
        <div class="envelope" id="envelope9">
            <div class="conteudo">
                <p><strong>Carta 9:</strong> por enquanto é isso totosa, por enquanto, isso ate eu fazer outra coisinha pq quando te ver tenho mais supresinhas so q sao materiais.</p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope9')">Abrir Carta</button>

        <!-- Carta 10 -->
        <div class="envelope" id="envelope10">
            <div class="conteudo">
                <p><strong>Carta 10:</strong> apartir do momento q vc ler nao tem como desler oq ja está lido, pois agora vc me deve uma têtê foto faz tempo q to sem, to quase desfalecendo sem meus têtê.</p>
            </div>
        </div>
        <button class="botao-abrir" onclick="abrirEnvelope('envelope10')">Abrir Carta</button>
    </div>

    <script>
        function abrirEnvelope(id) {
            const envelope = document.getElementById(id);
            envelope.classList.toggle('aberto');

            // Função para gerar corações
            gerarCoracoes();
        }

        function gerarCoracoes() {
            for (let i = 0; i < 10; i++) { // Gera 10 corações por vez
                const heart = document.createElement('div');
                heart.className = 'heart';
                // Coloca os corações em posições aleatórias ao longo da tela
                heart.style.left = `${Math.random() * 100}%`;

                document.body.appendChild(heart);

                // Remove o coração após a animação de queda
                setTimeout(() => {
                    heart.remove();
                }, 2000); // Duração da animação
            }
        }
    </script>

</body>
</html>
