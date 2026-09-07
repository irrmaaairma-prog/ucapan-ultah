# ucapan-ultah
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PERINGATAN DARURAT: KAMU TUA! 🚨</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            background: #ff7675;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            font-family: 'Impact', 'Arial Black', sans-serif;
            text-align: center;
            overflow: hidden;
            transition: background 0.5s;
        }
        .container {
            width: 90%;
            max-width: 450px;
            background: #fdcb6e;
            padding: 40px 20px;
            border-radius: 0px; /* Desain kaku biar keliatan panik */
            border: 8px solid #2d3436;
            box-shadow: 15px 15px 0px #2d3436;
            z-index: 10;
        }
        .emoji-kocak {
            font-size: 5rem;
            animation: mutar 0.5s infinite linear;
        }
        h1 {
            color: #2d3436;
            font-size: 2rem;
            text-transform: uppercase;
            margin: 20px 0;
            letter-spacing: 1px;
        }
        .p-lucu {
            font-family: 'Courier New', Courier, monospace;
            font-weight: bold;
            color: #2d3436;
            font-size: 1.1rem;
            margin-bottom: 20px;
        }
        .btn-wrapper {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
            height: 60px;
            position: relative;
        }
        button {
            padding: 10px 25px;
            font-size: 1.2rem;
            font-family: 'Impact', sans-serif;
            text-transform: uppercase;
            cursor: pointer;
            border: 4px solid #2d3436;
            box-shadow: 5px 5px 0px #2d3436;
            transition: 0.1s;
        }
        #btnMau {
            background-color: #00b894;
            color: white;
        }
        #btnMau:active {
            transform: translate(5px, 5px);
            box-shadow: none;
        }
        #btnGak {
            background-color: #d63031;
            color: white;
            position: absolute;
            left: 55%;
        }
        /* Konten Ucapan Lucu */
        .konten-rahasia {
            display: none;
            background: #fff;
            border: 4px solid #2d3436;
            padding: 20px;
            text-align: left;
            font-family: 'Arial', sans-serif;
            font-size: 1.05rem;
            line-height: 1.6;
            color: #2d3436;
            box-shadow: inset 5px 5px 0px #ffeaa7;
        }
        .konten-rahasia p {
            margin-bottom: 15px;
        }
        /* Efek Hujan Sampah/Emoji Lucu */
        .benda-jatuh {
            position: absolute;
            top: -60px;
            font-size: 2.5rem;
            pointer-events: none;
            animation: terjunUp 4s linear infinite;
        }
        @keyframes mutar {
            100% { transform: rotate(360deg); }
        }
        @keyframes terjunUp {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(110vh) rotate(720deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="container" id="kotakUtama">
        <!-- TAMPILAN JAHIL AWAL -->
        <div id="tampilanAwal">
            <div class="emoji-kocak">🚨</div>
            <h1>Sistem Mendeteksi Umur Anda Bertambah Tua Hari Ini!</h1>
            <p class="p-lucu">Mau menerima kenyataan pahit ini?</p>
            <div class="btn-wrapper">
                <button id="btnMau" onclick="terimaKenyataan()">Iya Pasrah</button>
                <!-- Tombol Gak Mau yang lari kalau didekati -->
                <button id="btnGak" onmouseover="lariLu()" onclick="pencetGakBisa()">Gak Mau!</button>
            </div>
        </div>

        <!-- TAMPILAN UCAPAN KOCAK -->
        <div id="tampilanUcapan" class="konten-rahasia">
            <p><strong>Cieeee, kuotanya di bumi berkurang setahun! 🫵🤣</strong></p>
            <p>Selamat bertambah tua ya! Gimana rasanya? Sudah mulai ngerasain encok, pegal linu, atau tiba-tiba pengen beli minyak angin gak kalau kena angin malam? Wajar kok, faktor usia, hehe.</p>
            <p>Doaku nggak muluk-muluk buat kamu di tahun ini:</p>
            <p>💸 Semoga rezekimu lancar biar bisa traktir aku makan enak (ini wajib, gak boleh pura-pura amnesia!).<br>
               🧠 Semoga makin dewasa dan gak hobi ngambek gak jelas lagi.<br>
               🔋 Semoga kuat begadang tapi mukanya gak mirip zombi pas pagi hari.</p>
            <p>Sudah ya, selamat merayakan hari menua nasional khusus buat kamu. Pokoknya buruan kirim emot 🍗🍕 ke WA-ku sebagai jaminan traktiran!</p>
        </div>
    </div>

    <script>
        // Fungsi membuat tombol "Gak Mau" lari acak
        function lariLu() {
            const btnGak = document.getElementById('btnGak');
            const randomX = Math.floor(Math.random() * 260) - 130; 
            const randomY = Math.floor(Math.random() * 180) - 90;  
            btnGak.style.transform = `translate(${randomX}px, ${randomY}px)`;
        }

        // Kalau mereka super cepat dan berhasil klik tombol "Gak Mau"
        function pencetGakBisa() {
            alert("Eits, gak bisa kabur dari kenyataan! Klik 'Iya Pasrah' aja sana! 😜");
            lariLu();
        }

        // Fungsi ketika tombol "Iya Pasrah" diklik
        function terimaKenyataan() {
            document.getElementById('tampilanAwal').style.display = 'none';
            document.getElementById('tampilanUcapan').style.display = 'block';
            
            // Ubah tema jadi warna hijau absurd
            document.body.style.background = '#00cec9'; 
            document.getElementById('kotakUtama').style.background = '#a29bfe';
            
            // Hujan emoji kocak dimulai
            setInterval(hujanEmojiReceh, 250);
        }

        // Efek hujan emoji komedi
        function hujanEmojiReceh() {
            const listEmoji = ['🤡', '💩', '🍗', '🦖', '💸', '👴', '👵', '🤣', '🩹'];
            const elemen = document.createElement('div');
            elemen.classList.add('benda-jatuh');
            
            elemen.innerText = listEmoji[Math.floor(Math.random() * listEmoji.length)];
            elemen.style.left = Math.random() * 100 + 'vw';
            elemen.style.animationDuration = (Math.random() * 1.5 + 2) + 's';
            elemen.style.fontSize = (Math.random() * 1.5 + 1.5) + 'rem';
            
            document.body.appendChild(elemen);
            
            setTimeout(() => {
                elemen.remove();
            }, 4000);
        }
    </script>

</body>
</html>
