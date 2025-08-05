# sicehan
sicehan

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página com Botões Interativos</title>
    <style>
        /* Estilos globais para o corpo da página */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh; /* Garante que a página ocupe toda a altura da viewport */
            background-color: #e9ecef; /* Cor de fundo suave */
            margin: 0;
            padding: 20px;
            box-sizing: border-box;
            color: #343a40;
        }

        /* Contêiner para os botões */
        .button-container {
            display: grid;
            /* Cria um layout de grade responsivo: */
            /* - auto-fit: Preenche o espaço disponível com o máximo de colunas. */
            /* - minmax(180px, 1fr): Cada coluna terá no mínimo 180px e no máximo 1 parte do espaço disponível. */
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px; /* Espaçamento entre os botões */
            max-width: 1200px; /* Largura máxima do contêiner */
            width: 100%; /* Ocupa 100% da largura disponível até o max-width */
            padding: 30px;
            background-color: #ffffff; /* Fundo branco para o contêiner */
            border-radius: 12px; /* Cantos arredondados */
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1); /* Sombra sutil */
        }

        /* Estilo base para todos os botões */
        .styled-button {
            background-color: #007bff; /* Cor azul primária */
            color: white; /* Texto branco */
            padding: 15px 25px; /* Espaçamento interno */
            border: none; /* Sem borda */
            border-radius: 8px; /* Cantos levemente arredondados */
            cursor: pointer; /* Muda o cursor para indicar que é clicável */
            font-size: 1.1em; /* Tamanho da fonte */
            font-weight: 600; /* Negrito */
            text-align: center;
            text-decoration: none; /* Remove sublinhado se for um link (embora seja um botão) */
            display: block; /* Ocupa a largura total da célula da grade */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Sombra para profundidade */
            /* Transições suaves para as propriedades de cor e transformação */
            transition: background-color 0.3s ease, color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
        }

        /* Estilo do botão ao passar o mouse (hover) */
        .styled-button:hover {
            background-color: #0056b3; /* Azul mais escuro ao passar o mouse */
            color: #e0e0e0; /* Cor do texto levemente alterada */
            transform: translateY(-3px); /* Leve elevação para um efeito interativo */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15); /* Sombra mais pronunciada */
        }

        /* Estilo do botão ao ser clicado (active) */
        .styled-button:active {
            transform: translateY(0); /* Volta à posição original */
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Sombra mais suave */
        }
    </style>
</head>
<body>
    <div class="button-container">
        <!-- Exemplo de 12 botões. Você pode alterar os nomes e os URLs. -->
        <button class="styled-button" onclick="openPage('https://www.google.com')">🔍 Buscar no Google</button>
        <button class="styled-button" onclick="openPage('https://www.youtube.com')">▶️ Ver Vídeos no YouTube</button>
        <button class="styled-button" onclick="openPage('https://www.wikipedia.org')">📚 Consultar Wikipedia</button>
        <button class="styled-button" onclick="openPage('https://www.github.com')">💻 Acessar GitHub</button>
        <button class="styled-button" onclick="openPage('https://www.facebook.com')">👍 Ir para o Facebook</button>
        <button class="styled-button" onclick="openPage('https://www.twitter.com')">🐦 Navegar no X (Twitter)</button>
        <button class="styled-button" onclick="openPage('https://www.linkedin.com')">🔗 Conectar no LinkedIn</button>
        <button class="styled-button" onclick="openPage('https://www.reddit.com')">💬 Explorar Reddit</button>
        <button class="styled-button" onclick="openPage('https://www.amazon.com')">🛒 Comprar na Amazon</button>
        <button class="styled-button" onclick="openPage('https://www.netflix.com')">🎬 Assistir Netflix</button>
        <button class="styled-button" onclick="openPage('https://www.spotify.com')">🎵 Ouvir Spotify</button>
        <button class="styled-button" onclick="openPage('https://www.microsoft.com')">🖥️ Visitar Microsoft</button>
    </div>

    <script>
        /**
         * Função JavaScript para abrir uma URL em uma nova aba do navegador.
         * @param {string} url - O endereço da página web a ser aberta.
         */
        function openPage(url) {
            window.open(url, '_blank'); // '_blank' garante que a página abra em uma nova aba/janela
        }
    </script>
</body>
</html>
