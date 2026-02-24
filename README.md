<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Corinthians - O Poderoso Timão</title>
    <style>
        /* --- ESTILO (CSS) --- */
        :root {
            --cor-fundo: #ffffff;
            --cor-texto: #1a1a1a;
            --cor-destaque: #000000;
            --borda: #dddddd;
            --sombra: rgba(0, 0, 0, 0.1);
        }

        /* Classe ativada pelo JavaScript */
        .dark-mode {
            --cor-fundo: #121212;
            --cor-texto: #ffffff;
            --cor-destaque: #ffffff;
            --borda: #333333;
            --sombra: rgba(255, 255, 255, 0.05);
        }

        body {
            background-color: var(--cor-fundo);
            color: var(--cor-texto);
            font-family: 'Segoe UI', Roboto, sans-serif;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            transition: background 0.4s ease, color 0.4s ease;
        }

        .container {
            text-align: center;
            padding: 40px;
            border: 2px solid var(--borda);
            border-radius: 20px;
            box-shadow: 0 10px 30px var(--sombra);
            max-width: 400px;
            background-color: var(--cor-fundo);
        }

        .escudo {
            width: 120px;
            margin-bottom: 20px;
            cursor: pointer;
            transition: transform 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .escudo:hover {
            transform: scale(1.2) rotate(10deg);
        }

        h1 {
            margin: 10px 0;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        p {
            font-style: italic;
            opacity: 0.8;
        }

        .btn-tema {
            margin-top: 30px;
            padding: 12px 25px;
            background-color: var(--cor-destaque);
            color: var(--cor-fundo);
            border: none;
            border-radius: 50px;
            font-weight: bold;
            cursor: pointer;
            text-transform: uppercase;
            transition: opacity 0.2s;
        }

        .btn-tema:hover {
            opacity: 0.8;
        }

        footer {
            margin-top: 20px;
            font-size: 0.8rem;
        }
    </style>
</head>
<body>

    <div class="container">
        <img src="https://upload.wikimedia.org/wikipedia/pt/b/b4/Corinthians_simbolo.png" 
             alt="Escudo do Corinthians" class="escudo" id="logo">
        
        <h1>Corinthians</h1>
        <p>"Salve o Corinthians, o campeão dos campeões!"</p>

        <div id="status-torcedor">
            <strong>Status:</strong> <span id="msg">Lutando até o fim!</span>
        </div>

        <button class="btn-tema" id="toggle-btn">Mudar para Modo Escuro</button>

        <footer>Criado pela Fiel Torcida 🦅</footer>
    </div>

    <script>
        const btn = document.getElementById('toggle-btn');
        const body = document.body;
        const logo = document.getElementById('logo');
        const msg = document.getElementById('msg');

        // Evento de clique para mudar o tema
        btn.addEventListener('click', () => {
            body.classList.toggle('dark-mode');

            // Lógica para atualizar o texto do botão e a mensagem
            if (body.classList.contains('dark-mode')) {
                btn.innerText = 'Mudar para Modo Claro';
                msg.innerText = 'É sangue no olho, é tapa na orelha!';
                msg.style.color = '#fff';
            } else {
                btn.innerText = 'Mudar para Modo Escuro';
                msg.innerText = 'Lutando até o fim!';
                msg.style.color = '#000';
            }
        });

        // Pequeno "easter egg" ao clicar no escudo
        logo.addEventListener('click', () => {
            alert("VAI CORINTHIANS! 🦅🏴🏳️");
        });

        // Mensagem no console para os curiosos
        console.log("%c 1910 - Corinthians ", "color: white; background: black; font-weight: bold; padding: 5px;");
    </script>
</body>
</html>
