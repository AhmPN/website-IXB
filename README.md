
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Website Kelas 9B</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #fff6ec;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #a0522d;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      background-color: #f5d5a1;
      padding: 10px;
      text-align: center;
    }
    .menu-btn {
      margin: 6px;
      padding: 10px 18px;
      background-color: #f0c38e;
      border: none;
      border-radius: 12px;
      font-weight: bold;
      cursor: pointer;
    }
    .menu-btn:hover {
      background-color: #dfa96b;
    }
    #content {
      padding: 25px;
      background-color: #fffdf8;
      min-height: 300px;
    }
    footer {
      background-color: #a0522d;
      color: white;
      text-align: center;
      padding: 15px;
    }
    footer a {
      color: #ffffff;
      font-weight: bold;
      text-decoration: none;
      margin: 0 10px;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 10px;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 8px;
      text-align: center;
    }
  </style>
</head>
<body>

<header>
  <h1>SMPN 1 PANGKALAN LADA</h1>
  <h2>Website Kelas 9B</h2>
</header>

<nav>
  <button class="menu-btn" onclick="showContent('struktur')">Struktur Kelas</button>
  <button class="menu-btn" onclick="showContent('anggota')">Anggota Siswa</button>
  <button class="menu-btn" onclick="showContent('tata')">Tata Tertib</button>
  <button class="menu-btn" onclick="showContent('kebersihan')">Peraturan Kebersihan</button>
  <button class="menu-btn" onclick="showContent('pelajaran')">Jadwal Pelajaran</button>
  <button class="menu-btn" onclick="showContent('piket')">Jadwal Piket</button>
  <button class="menu-btn" onclick="showContent('pr')">Tugas / PR</button>
  <button class="menu-btn" onclick="showContent('galeri')">Galeri Foto</button>
</nav>

<div id="content">
  <h2>Selamat datang di Website Kelas 9B!</h2>
  <p>Klik menu di atas untuk melihat informasi penting dan seru seputar kelas kita 😊</p>
</div>

<footer>
  <p>Website Kelas 9B | Designed by: APutraN</p>
  <p>
    <a href="https://www.instagram.com/onebraderclass?igsh=dmIydWc1aG50aWdy" target="_blank">Instagram</a> |
    <a href="https://www.tiktok.com/@asixxbee6?_t=ZS-8xULIQm8QXR&_r=1" target="_blank">TikTok</a>
  </p>
</footer>

<script>
  function showContent(menu) {
    const content = {
      struktur: `
        <h2>Struktur Kelas 9B</h2>
        <ul>
          <h3>Wlali Kelas : akan hadir</h3>
          <li>Ketua Kelas: Akan Hadir</li>
          <li>Wakil Ketua: Akan Hadir</li>
          <li>Sekretaris 1: Akan Hadir</li>
          <li>Sekretaris 2: Akan Hadir</li>
          <li>Bendahara 1: Akan Hadir</li>
          <li>Bendahara 2: Akan Hadir</li>
        </ul>
      `,
      anggota: `
        <h2>Daftar Anggota Siswa Kelas 9B (32 Siswa)</h2>
        <ol>
          <li>Adelia Ainun Zakia</li>
          <li>Adinda Selmi Yusfita</li>
          <li>Ahmad Putra Nurrohim</li>
          <li>Alisia Jastin</li>
          <li>Amelia Nur Rahmadani</li>
          <li>Anita Sulfania</li>
          <li>Cahya Nengrum Aulia Ulfah</li>
          <li>Choliv Fuadiya</li>
          <li>Dafi Idriansyah</li>
          <li>Devi Nur Maulidda</li>
          <li>Dewi Audray Agdiningviar</li>
          <li>Dimas Surya Irawan</li>
          <li>Dira Hadi Erwanto</li>
          <li>Dwi Irji Febiana</li>
          <li>Edo Hariyadi</li>
          <li>Erwin Alfiromdoni</li>
          <li>Imana Pungky Mavano</li>
          <li>Micko Maulana</li>
          <li>Muhamad Azriel Ardianta</li>
          <li>Muhamad Fahmy Ferdiansyah</li>
          <li>Muhamad Farras Ahsanul Huda</li>
          <li>Muhammad Arjuna Muarif Salam</li>
          <li>Muhammad Rishad Tabatala Arsodiq</li>
          <li>Mutiara Dwi Febrianti</li>
          <li>Nabila Azzahra</li>
          <li>Nur Sabrina</li>
          <li>Putri Nur Ainiyyah Zahraa</li>
          <li>Riyo Ramadhani</li>
          <li>Silda Simatus Zahro</li>
          <li>Sintia Nabila</li>
          <li>Yogik Aditiyono</li>
          <li>Zaky Sofyan</li>
        </ol>
      `,
      tata: `
        <h2>Tata Tertib Kelas</h2>
        <ol>
          <li>Datang tepat waktu sebelum jam pelajaran dimulai.</li>
          <li>Berpakaian rapi dan sesuai peraturan sekolah.</li>
          <li>Berperilaku sopan terhadap guru dan teman.</li>
          <li>Menjaga kebersihan dan kerapihan kelas.</li>
        </ol>
      `,
      kebersihan: `
        <h2>Peraturan Kebersihan Kelas</h2>
        <ul>
          <li>Buang sampah pada tempatnya.</li>
          <li>Dilarang makan/minum di dalam kelas saat pelajaran berlangsung.</li>
          <li>Petugas piket wajib menyapu dan merapikan kelas setiap pagi dan sebelum pulang sekolah.</li>
        </ul>
      `,
      pelajaran: `
        <h2>Jadwal Pelajaran Kelas 9B</h2>
        <table>
          <tr><th>Hari</th><th>Mata Pelajaran</th></tr>
          <tr><td>Senin</td><td>Segera Hadir</td></tr>
          <tr><td>Selasa</td><td>Segera Hadir</td></tr>
          <tr><td>Rabu</td><td>Segera Hadir</td></tr>
          <tr><td>Kamis</td><td>Segera Hadir</td></tr>
          <tr><td>Jumat</td><td>Segera Hadir</td></tr>
          <tr><td>Sabtu</td><td>P5,P5,P5</td></tr>
        </table>
      `,
      piket: `
        <h2>Jadwal Piket Mingguan</h2>
        <table>
          <tr><th>Hari</th><th>Nama Petugas</th></tr>
          <tr><td>Senin</td><td>Segera Hadir</td></tr>
          <tr><td>Selasa</td><td>Segera Hadir</td></tr>
          <tr><td>Rabu</td><td>Segera Hadir</td></tr>
          <tr><td>Kamis</td><td>Segera Hadir</td></tr>
          <tr><td>Jumat</td><td>Segera Hadir</td></tr>
          <tr><td>Sabtu</td><td>Segera Hadir</td></tr>
        </table>
      `,
      pr: `
        <h2>Tugas / PR Terbaru</h2>
        <ul>
          <li>Matematika: segera hadir</li>
          <li>IPA: segera hadir</li>
          <li>PKN: segera hadir</li>
        </ul>
      `,
      galeri: `
        <h2>Galeri Foto & Kenangan</h2>
        <img src="fotoulangan.jpg" style="width:100%; border-radius:10px;">
        <p>📸 foto ulangan hari ke 2 😍</p>
        <img src="persiapanupacara.jpg" style="width:100%; border-radius:10px;">
        <p>📸 foto persiapan upacara 😍</p>
        <img src="upacara1.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah upacara 😍</p>
        <img src="upacara2.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah upacara 😍</p>
        <img src="upacara3.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah upacara 😍</p>
        <img src="kemah1.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar cewek cantik 8b 😍</p>
        <img src="kemah2.jpg" style="width:100%; border-radius:10px;">
        <p>📸 Arjuna kecapean makan 🤣🤣</p>
        <img src="kemah3.jpg" style="width:100%; border-radius:10px;">
        <p>📸 foto laki" ngerumpi😍</p>
        <img src="kemah4.jpg" style="width:100%; border-radius:10px;">
        <p>📸  cewek nya makan, cowok nya yang masak 😅</p>
        <img src="tarian1.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah tampil menari 😍</p>
        <img src="ibul.jpg" style="width:100%; border-radius:10px;">
        <p>📸 foto bersama Ibu Laila 😍😍</p>
        
      `
    };

    document.getElementById("content").innerHTML = content[menu] || "<p>Menu belum tersedia.</p>";
  }
</script>

</body>
</html>
