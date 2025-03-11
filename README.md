<!DOCTYPE html>
<html>
<head>
    <title>Ajak Pacaran 💕</title>
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/brython/3.9.5/brython.min.js"></script>
</head>
<body onload="brython()">
    <h2>💕 Hai, ada sesuatu yang ingin aku tanyakan... 💕</h2>
    <button onclick="tanya()">Klik di sini</button>
    <p id="hasil"></p>

    <script type="text/python">
        from browser import document, html

        def tanya(event):
            jawaban = window.prompt("Maukah kamu menjadi pacarku? 😊 (Ya/Tidak)")
            if jawaban.lower() == "ya":
                document["hasil"].text = "😍 Yeay! Aku sangat bahagia! ❤️"
            elif jawaban.lower() == "tidak":
                document["hasil"].text = "😢 Aku mengerti... Semoga kita tetap bisa berteman! 💙"
            else:
                document["hasil"].text = "🤔 Aku anggap itu sebagai 'mungkin'. 😉"

        document["tanya"] = tanya
    </script>
</body>
</html>
