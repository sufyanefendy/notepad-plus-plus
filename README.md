<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Game Tebak Angka</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      margin: 5px;
    }
  </style>
</head>
<body>
  <h1>Game Tebak Angka</h1>
  <p>Komputer telah memilih angka antara <strong>1 - 10</strong>.</p>
  <input type="number" id="tebakan" min="1" max="10" placeholder="Tebak angkanya" />
  <button onclick="cekTebakan()">Cek</button>
  <p id="hasil"></p>

  <script>
    const angkaBenar = Math.floor(Math.random() * 10) + 1;

    function cekTebakan() {
      const input = document.getElementById("tebakan").value;
      const hasil = document.getElementById("hasil");

      if (input == angkaBenar) {
        hasil.innerText = "🎉 Selamat! Kamu benar!";
      } else {
        hasil.innerText = "❌ Salah! Coba lagi!";
      }
    }
  </script>
</body>
</html>
