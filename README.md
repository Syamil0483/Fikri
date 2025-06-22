<Seru-seruan>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sebuah Ruang Lucu untuk Kita</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&display=swap');

    body {
      margin: 0;
      font-family: 'Comic Neue', cursive;
      background-color: #fff0f5;
      color: #444;
      overflow-x: hidden;
    }

    .container {
      max-width: 700px;
      margin: 30px auto;
      background-color: #fff;
      padding: 30px 25px;
      border-radius: 25px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
      animation: fadeIn 1s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    header {
      text-align: center;
    }

    header img {
      max-width: 140px;
      border-radius: 20px;
      margin-bottom: 15px;
    }

    h1 {
      color: #d63384;
      font-size: 26px;
      margin-bottom: 10px;
    }

    p {
      font-size: 16px;
      color: #555;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
      flex-wrap: wrap;
    }

    .buttons button {
      padding: 12px 22px;
      font-size: 15px;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    #yesButton {
      background-color: #ff69b4;
      color: white;
      box-shadow: 0 3px 6px rgba(0,0,0,0.1);
    }

    #noButton {
      background-color: #ffe4e1;
      color: #d6336c;
      position: relative;
    }

    #noButton:hover {
      transform: scale(1.1);
    }

    #formContainer {
      display: none;
      max-height: 80vh;
      overflow-y: auto;
      scroll-behavior: smooth;
    }

    .question-block {
      margin-bottom: 25px;
    }

    label {
      display: block;
      font-weight: bold;
      margin-bottom: 8px;
      color: #d6336c;
      font-size: 16px;
    }

    textarea {
      width: 100%;
      padding: 10px;
      border-radius: 12px;
      border: 1px solid #ccc;
      font-size: 15px;
      resize: vertical;
      box-shadow: inset 0 1px 3px rgba(0,0,0,0.05);
      font-family: 'Comic Neue', cursive;
    }

    .navigation-buttons {
      display: flex;
      justify-content: space-between;
      margin-top: 25px;
    }

    .nav-button {
      padding: 12px 24px;
      font-size: 15px;
      font-weight: bold;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      background-color: #f8bbd0;
      color: #880e4f;
      transition: background 0.2s;
    }

    .nav-button:hover {
      background-color: #f48fb1;
    }

    button[type="submit"] {
      display: block;
      width: 100%;
      margin-top: 30px;
      padding: 15px;
      font-size: 17px;
      font-weight: bold;
      color: white;
      background: linear-gradient(to right, #ec407a, #d81b60);
      border: none;
      border-radius: 20px;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(0,0,0,0.15);
    }

    button[type="submit"]:hover {
      transform: scale(1.03);
    }

    .page {
      display: none;
    }

    .page.active {
      display: block;
    }
  </style>
</head>
<body>

  <!-- HALAMAN INTRO -->
  <div class="container" id="introContainer">
    <header>
      <img src="https://media.tenor.com/gUiu1zyxfzYAAAAi/bear-kiss-bear-kisses.gif" alt="Cute Bear" />
      <h1>Hai Intan Sayangg 🧸💕</h1>
      <p>Mau isi-isi sesuatu buat aku nggak? Lucu-lucuan ajaaa 😚</p>
    </header>
    <div class="buttons">
      <button id="yesButton">Iyaa kenapaa sayaang? 😍</button>
      <button id="noButton">Gmw ah, malas 🙄</button>
    </div>
  </div>

  <!-- HALAMAN FORM DEEPTALK -->
  <div class="container" id="formContainer">
    <header>
      <img src="https://media.tenor.com/D15-kH_3WwEAAAAi/love-letter.gif" alt="Love Letter">
      <h1>Deeptalk Bareng Intan ❤️</h1>
      <p>Ayo ngobrol dari hati ke hati yaa 😚 Semua jawabanmu aman di aku kok!</p>
    </header>

    <form action="https://formspree.io/f/xanjdrpq" method="POST">
      <div id="page-1" class="page active">
        <div class="question-block">
          <label>1. Apa hal yang paling bikin kamu bersyukur kita bareng?</label>
          <textarea name="1_syukur"></textarea>
        </div>
        <div class="question-block">
          <label>2. Satu sifat aku yang paling kamu sukaa?</label>
          <textarea name="2_sifat_favorit"></textarea>
        </div>
        <div class="question-block">
          <label>3. Kapan kamu ngerasa paling dicintai?</label>
          <textarea name="3_dicintai"></textarea>
        </div>
        <div class="question-block">
          <label>4. Gambaran masa depan kita menurut kamu?</label>
          <textarea name="4_masa_depan"></textarea>
        </div>
      </div>

      <div id="page-2" class="page">
        <div class="question-block">
          <label>5. Apa yang bisa bikin kita makin lengket?</label>
          <textarea name="5_lengket"></textarea>
        </div>
        <div class="question-block">
          <label>6. Hal yang kamu takutin dalam hubungan kita?</label>
          <textarea name="6_takut"></textarea>
        </div>
        <div class="question-block">
          <label>7. Ide lucu supaya makin klik?</label>
          <textarea name="7_lucu"></textarea>
        </div>
        <div class="question-block">
          <label>8. Cara kita tetap mesra walau udah lama?</label>
          <textarea name="8_mesra"></textarea>
        </div>
      </div>

      <!-- Navigasi -->
      <div class="navigation-buttons">
        <button type="button" id="prevBtn" class="nav-button">⏮ Sebelumnya</button>
        <button type="button" id="nextBtn" class="nav-button">Lanjut ⏭</button>
      </div>

      <button type="submit">Kirim ke Sayangg! 💌</button>
    </form>
  </div>

  <script>
    const yesButton = document.getElementById('yesButton');
    const noButton = document.getElementById('noButton');
    const introContainer = document.getElementById('introContainer');
    const formContainer = document.getElementById('formContainer');

    yesButton.addEventListener('click', () => {
      introContainer.style.display = 'none';
      formContainer.style.display = 'block';
    });

    noButton.addEventListener('mouseover', () => {
      const i = Math.floor(Math.random() * (window.innerWidth - noButton.offsetWidth));
      const j = Math.floor(Math.random() * (window.innerHeight - noButton.offsetHeight));
      noButton.style.position = 'absolute';
      noButton.style.left = i + 'px';
      noButton.style.top = j + 'px';
    });

    // Navigasi halaman
    let currentPage = 1;
    const totalPages = 2;

    function showPage(num) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById(`page-${num}`).classList.add('active');
      document.getElementById('prevBtn').style.display = num === 1 ? 'none' : 'inline-block';
      document.getElementById('nextBtn').style.display = num === totalPages ? 'none' : 'inline-block';
    }

    document.getElementById('nextBtn').addEventListener('click', () => {
      if (currentPage < totalPages) {
        currentPage++;
        showPage(currentPage);
      }
    });

    document.getElementById('prevBtn').addEventListener('click', () => {
      if (currentPage > 1) {
        currentPage--;
        showPage(currentPage);
      }
    });

    showPage(currentPage);
  </script>
</body>
</html>
