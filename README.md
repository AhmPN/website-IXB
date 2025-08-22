
<head>
  <meta charset="UTF-8">
  <title>Website Kelas IX-B</title>
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
  <h2>Website Kelas IXB</h2>
  <html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Tanggal & Waktu</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #fdfcfb;
      margin-top: 50px;
    }
    #waktu {
      font-size: 15px;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>
  <div id="waktu"></div>
  <script>
    function updateWaktu() {
      const hariNama = ["Minggu","Senin","Selasa","Rabu","Kamis","Jumat","Sabtu"];
      const bulanNama = ["Januari","Februari","Maret","April","Mei","Juni",
                         "Juli","Agustus","September","Oktober","November","Desember"];
      let sekarang = new Date();
      let hari = hariNama[sekarang.getDay()];
      let tanggal = sekarang.getDate();
      let bulan = bulanNama[sekarang.getMonth()];
      let tahun = sekarang.getFullYear();
      let jam = String(sekarang.getHours()).padStart(2, '0');
      let menit = String(sekarang.getMinutes()).padStart(2, '0');
      let detik = String(sekarang.getSeconds()).padStart(2, '0');
      document.getElementById("waktu").innerHTML =
        `${hari}, ${tanggal} ${bulan} ${tahun} | ${jam}:${menit}:${detik}`;
    }
    setInterval(updateWaktu, 1000);
    updateWaktu();
  </script>
</body>
</html>
</header>
<nav>
  <button class="menu-btn" onclick="showContent('pesan')">Tulis Pesan</button>
  <button class="menu-btn" onclick="showContent('struktur')">Struktur Kelas</button>
  <button class="menu-btn" onclick="showContent('anggota')">Anggota Siswa</button>
  <button class="menu-btn" onclick="showContent('tata')">Tata Tertib Kelas</button>
  <button class="menu-btn" onclick="showContent('kebersihan')">Peraturan Kebersihan</button>
  <button class="menu-btn" onclick="showContent('pelajaran')">Jadwal Pelajaran</button>
  <button class="menu-btn" onclick="showContent('piket')">Jadwal Piket</button>
  <button class="menu-btn" onclick="showContent('pr')">Tugas / PR</button>
  <button class="menu-btn" onclick="showContent('galeri')">Galeri Foto</button>
</nav>
<div id="content">
  <h2>Selamat datang di Website Kelas IX-B!</h2>
  <p>Klik di atas untuk melihat informasi penting dan seru seputar kelas kita 😊</p>
</div>
<footer>
  <p>Website Kelas IXB | Designed by: APutraN</p>
  <p>
    <!-- Tambahkan link Font Awesome di bagian <head> -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
        <a href="https://www.instagram.com/ofc.songobhee9?igsh=MTFmeTdrazB1dXd5NA" target="_blank" style="margin: 0 10px; text-decoration: none; color: #E1306C;">
            <i class="fab fa-instagram"></i> Instagram
        </a>
        <a href="https://www.tiktok.com/@asixxbee6?_t=ZS-8xULIQm8QXR&_r=1" target="_blank" style="margin: 0 10px; text-decoration: none; color: #000;">
            <i class="fab fa-tiktok"></i> TikTok
        </a>
    </p>
</footer>
<script>
  function showContent(menu) {
    const content = {
      pesan: `
        <div id="content">
  <section id="pengaduan">
  <h2>Tulis Pesan Untuk Kelas IX-B</h2>
  <p>Silakan isi form di bawah untuk menyampaikan pesan. Klik 2x untuk mengirim pesan.</p>
  <form action="https://formsubmit.co/ahmadputra.nur31@GMAIL.COM" method="POST"
        style="max-width:450px; margin:auto; background:#f9f9f9; padding:20px; border-radius:15px; box-shadow:0 4px 12px rgba(0,0,0,0.1);">    
    <label>Nama:</label><br>
    <input type="text" name="nama" required 
           style="width:100%; padding:10px; margin:8px 0; border-radius:10px; border:1px solid #ccc;"><br>   
    <label>Tulis Pesan:</label><br>
    <textarea name="pesan" required 
              style="width:100%; padding:10px; margin:8px 0; border-radius:10px; border:1px solid #ccc;" rows="4"></textarea><br>   
    <!-- Setting tambahan -->
    <input type="hidden" name="_captcha" value="false"> <!-- biar gak ada captcha -->
    <input type="hidden" name="_template" value="table"> <!-- email tampil lebih rapi -->
    <input type="hidden" name="_subject" value="Pengaduan Baru dari Website Kelas IX-B"> <!-- judul email -->    
    <button type="submit" 
            style="padding:12px 20px; background:#2196f3; color:white; border:none; border-radius:10px; font-weight:bold; cursor:pointer;">
      Kirim Pesan 📧
    </button>
  </form>
</section>
      `,
      struktur: `
        <h2>Struktur Kelas IX-B</h2>
        <ul>
          <h3>Wali Kelas : Musringatun,S.Pd.I.</h3>
          <li>Ketua Kelas: Ahmad Putra Nurrohim</li>
          <li>Wakil Ketua: Zaky Sofyan</li>
          <li>Sekretaris 1: Amelia Nur R</li>
          <li>Sekretaris 2: Adelia Ainun Z</li>
          <li>Bendahara 1: Devi Nur M</li>
          <li>Bendahara 2: Dewi Audray A</li>
          <li>Seksi Kerohanian 1: Nabila</Li>
          <li>Seksi Kerohanian 2: Dira</li>
          <li>Seksi Keamanan 1: Azriel</li>
          <li>Seksi Keamanan 2: Yogik</li>
          <li>Seksi Kebersihan 1: Dafi</li>
          <li>Seksi Kebersihan 2: Farras</li>
          <li>Seksi Kesehatan 1: Rishad</li>
          <li>Seksi Kesehatan 2: Riyo</li>
        </ul>
      `,
      anggota: `
        <h2>Daftar Anggota Siswa Kelas IX-B (32 Siswa)</h2>
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
          <li>Siswa wajib mengerjakan tugas yang diberikan kepada guru.</li>
          <li>Berpakaian rapi dan sesuai peraturan sekolah.</li>
          <li>Berperilaku sopan terhadap guru dan teman.</li>
          <li>dilarang makan/minum di dalam kelas saat pelajaran berlangsung.</li>
        </ol>
      `,
      kebersihan: `
        <h2>Peraturan Kebersihan Kelas</h2>
        <ul>
          <li>Buang sampah pada tempatnya.</li>
          <li>tidak mengotori kelas</li>
          <li>Petugas piket wajib menyapu dan merapikan kelas setiap pagi dan sebelum pulang sekolah.</li>
          <li>Petugas piket wajib lapor absen sebelum mulai pelajaran.</li>
        </ul>
      `,
      pelajaran: `
        <h2>Jadwal Pelajaran Kelas IX-B</h2>
        <table>
          <tr><th>Hari</th><th>Mata Pelajaran</th></tr>
          <tr><td>Senin</td><td>Bhs.Inggris, Pend.Pancasila, IPA</td></tr>
          <tr><td>Selasa</td><td>IPS, Informatika, Bhs.Indonesia</td></tr>
          <tr><td>Rabu</td><td>Pend.Agama, Matematika, Seni Budaya</td></tr>
          <tr><td>Kamis</td><td>PJOK, Matematika, Mulok, IPA</td></tr>
          <tr><td>Jumat</td><td>Bhs.Indonesia</td></tr>
          <tr><td>Sabtu</td><td>P5</td></tr>
        </table>
      `,
      piket: `
        <h2>Jadwal Piket Kelas IX-B</h2>
        <table>
          <tr><th>Hari</th><th>Nama Petugas</th></tr>
          <tr><td>Senin</td><td>Nabila, Silda, Adelia, Micko, Fahmi, Rishad</td></tr>
          <tr><td>Selasa</td><td>Sabrina, Sintia, Cahya, Putra, Dafi</td></tr>
          <tr><td>Rabu</td><td>Anitaaa, Dwi Irji, Mutiara, Azriel, Farras</td></tr>
          <tr><td>Kamis</td><td>Jastin, Zahraa, Dira, Pungky, Erwin</td></tr>
          <tr><td>Jumat</td><td>Devi, Amelia, Arjuna, Dimas, Riyo, Zaky</td></tr>
          <tr><td>Sabtu</td><td>Via, Choliv, Adinda, Edo, Yogik</td></tr>
        </table>
      `,
      pr: `     
        <h1>Tugas / PR Terbaru Jumat,22 08 2025</h1>
        <ul>
          <h2>Tidak Ada Tugas
        </ul>
        <div id="content">
  <section id="pengaduan">
  <h4>Tulis Pesan Untuk Menanyakan Tugas Jika Belum Mengerti</h4>
  <form action="https://formsubmit.co/ahmadputra.nur31@GMAIL.COM" method="POST"
        style="max-width:450px; margin:auto; background:#f9f9f9; padding:20px; border-radius:15px; box-shadow:0 4px 12px rgba(0,0,0,0.1);">    
    <label>Nama:</label><br>
    <input type="text" name="nama" required 
           style="width:100%; padding:10px; margin:8px 0; border-radius:10px; border:1px solid #ccc;"><br>    
    <label>Tulis Pesan:</label><br>
    <textarea name="pesan" required 
              style="width:100%; padding:10px; margin:8px 0; border-radius:10px; border:1px solid #ccc;" rows="4"></textarea><br>    
    <!-- Setting tambahan -->
    <input type="hidden" name="_captcha" value="false"> <!-- biar gak ada captcha -->
    <input type="hidden" name="_template" value="table"> <!-- email tampil lebih rapi -->
    <input type="hidden" name="_subject" value="Pengaduan Baru dari Website Kelas IX-B"> <!-- judul email -->    
    <button type="submit" 
            style="padding:12px 20px; background:#2196f3; color:white; border:none; border-radius:10px; font-weight:bold; cursor:pointer;">
      Kirim Pesan 📧
    </button>
  </form>
</section>
      `,
      galeri: `
        <h2>Galeri Foto & Kenangan</h2>
        <img src="fotoc2.jpg" style="width:100%; border-radius:10px;">
        <p>📷 foto bersama 😘
        <img src="fotoc1.jpg" style="width:100%; border-radius:10px;">
        <p>📷 foto bersama 😘
        <img src="fotoulangan.jpg" style="width:100%; border-radius:10px;">
        <p>📸 foto ulangan hari ke 2 😍</p>
        <img src="persiapanupacara.jpg" style="width:100%; border-radius:10px;">
        <p>📸 foto persiapan upacara 😍</p>
        <img src="upacara1.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah upacara bersama Ibu Yuni 😍</p>
        <img src="upacara2.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah upacara 😍</p>
        <img src="upacara3.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar setelah upacara 😍</p>
        <img src="kemah1.jpg" style="width:100%; border-radius:10px;">
        <p>📸 fotbar cewek cantik 8b 😍</p>
        <img src="kemah2.jpg" style="width:100%; border-radius:10px;">
        <p>📸 🤣🤣</p>
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
