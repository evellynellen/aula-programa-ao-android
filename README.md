# aula-programaçao-android

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="utf-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML5 – Estrutura básica</title>
    <style>
        body {
            background-color: rgb(105, 105, 173);
            color: white;
            font: normal 20pt Arial;
        }
    </style>
</head>
<body>

    <h1>Olá, mundo</h1>
    <p>Já me livrei da maldição</p>

    <!-- Adicionando um campo de entrada e um botão para processar o texto -->
    <h1>Processador de Texto</h1>
    <label for="inputString">Digite seu texto:</label>
    <input type="text" id="inputString" placeholder="Digite sua frase aqui">
    <button onclick="capitalizarPalavra()">Processar</button>
    <h2>Resultado</h2>
    <p id="outputString"></p>

    <script>
        // Função para capitalizar palavras com mais de dois caracteres
        function capitalizarPalavra() {
            const identificador = document.getElementById("inputString").value;
            const palavras = identificador.split(" "); // Divide o texto em palavras

            const resultado = palavras.map(palavra => {
                if (palavra.length > 2) {
                    return palavra.charAt(0).toUpperCase() + palavra.slice(1).toLowerCase();
                } else {
                    return palavra;
                }
            });

            document.getElementById("outputString").textContent = resultado.join(" ");
        }

        // Exibir alerta na página 
        window.alert('Minha primeira mensagem');
        // Botão de sim ou não
        window.confirm('Está gostando de JS?');
        // Pergunta 
        window.prompt('Qual é o seu nome?');
    </script>
</body>
</html>
