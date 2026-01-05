<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fashion Angola - Oficial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #fdfaf2;
            color: #3d2b1f;
            padding: 20px;
        }
        .logo-fa {
            width: 80px;
            height: 80px;
            background-color: #d4af37;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 24px;
            margin: 0 auto 20px;
        }
        .btn {
            display: block;
            width: 80%;
            max-width: 300px;
            margin: 15px auto;
            padding: 12px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 25px;
            transition: 0.3s;
        }
        /* Cores dos Botões */
        .btn-tiktok {
            background-color: #010101;
            color: white;
        }
        .btn-instagram {
            background-color: #E1306C;
            color: white;
        }
        .btn-whatsapp {
            background-color: #25D366;
            color: white;
        }
        .caixa-sorteio {
            border: 2px dashed #d4af37;
            border-radius: 15px;
            padding: 20px;
            margin-top: 30px;
            background-color: white;
        }
        input {
            width: 80%;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .btn-sortear {
            background-color: #d4af37;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <div class="logo-fa">FA</div>
    <h1>Fashion Angola</h1>
    <p>Bijuterias que realçam a tua beleza! ✨</p>

    <a href="https://www.tiktok.com/@sula.fashion5" class="btn btn-tiktok" target="_blank">Seguir no TikTok</a>
    
    <a href="https://www.instagram.com/sula.fashion5/" class="btn btn-instagram" target="_blank">Instagram</a>
    
    <a href="https://wa.me/244928185406" class="btn btn-whatsapp" target="_blank">Pedir pelo WhatsApp</a>

    <div class="caixa-sorteio">
        <h3>🎁 Sorteio para Seguidores</h3>
        <p>Cola os nomes separados por vírgula:</p>
        <input type="text" id="nomes" placeholder="Ex: Maria, Ana, Rosa">
        <br>
        <button class="btn-sortear" onclick="sortear()">SORTEAR AGORA</button>
        <div id="resultado" style="margin-top: 15px; font-weight: bold; color: #E1306C; font-size: 20px;"></div>
    </div>

    <script>
        function sortear() {
            let texto = document.getElementById('nomes').value;
            if (texto.trim() == "") {
                alert("Escreve os nomes primeiro!");
                return;
            }
            let lista = texto.split(',');
            let vencedor = lista[Math.floor(Math.random() * lista.length)];
            document.getElementById('resultado').innerText = "🎉 Vencedor(a): " + vencedor.trim();
        }
    </script>

</body>
</html>

