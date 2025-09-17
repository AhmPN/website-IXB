  
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

  <style>
    :root{
      --bg1: #a0522d;
      --bg2: #dfa96;
      --card: #ffffff;
      --line: #a0522d;
      --text: #2b2b2b;
      --muted: #555;
      --accent: #a0522d;
      --accent-2:#dfa96b;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(160deg, var(--bg1), var(--bg2));
      color:var(--text);
    }
    .page{
      max-width:1200px; margin-inline:auto; padding:0px; 
    }
    header{
      display:flex; align-items:center; justify-content:space-between; gap:0px; flex-wrap:wrap;
    }
    h1{font-size:clamp(1.2rem, 2vw + 0.8rem, 2rem); margin:0; letter-spacing:0.5px; color:var(--card)}
    .sub{color:var(--card); font-size:0.95rem}
    .controls{display:flex; gap:8px; flex-wrap:wrap}
    .btn{
      appearance:none; border:1px solid var(--line); background:#fff3;
      color:var(--card); padding:10px 14px; border-radius:14px; cursor:pointer; font-weight:600; 
      box-shadow:0 2px 6px rgba(0,0,0,0.2);
    }
    .btn:hover{background:#fff6}
    .btn:active{transform:translateY(1px)}.tree-wrapper{
  border:1px solid var(--line); box-shadow:0 10px 40px rgba(0,0,0,0.2) inset;
  overflow:auto;
}
.tree{ display:inline-blpadding:24px 18px; }
.tree ul{ padding-top:20px; position:relative; padding-left:0; text-align:center }
.tree li{ display:inline-block; vertical-align:top; list-style:none; position:relative; padding:20px 14px 0 14px; }
.tree li::before, .tree li::after{
  content:""; position:absolute; top:0; border-top:2px solid var(--line); width:50%; height:20px;
}
.tree li::before{ right:50%; }
.tree li::after{ left:50%; border-left:2px solid var(--line); }
.tree li:only-child::before, .tree li:only-child::after{ display:none; }
.tree li:only-child{ padding-top:0; }
.tree li:first-child::before{ border:none; }
.tree li:last-child::after{ border:none; }
.tree ul ul::before{
  content:""; position:absolute; top::2px solid var(--line); width:0; height:20px;
}
.node{
  background:var(--card);
  border:1px solid var(--line); color:var(--text); min-width:180px; max-width:240px;
  padding:12px 14px; border-radius:16px; text-align:center; display:grid; gap:6px;
  box-shadow:0 6px 18px rgba(0,0,0,0.2);
}
.node .role{ font-size:0.75rem; letter-spacing:0.3px; color:var(--accent); text-transform:uppercase; font-weight:800 }
.node .name{ font-size:1rem; font-weight:800 }
.node .meta{ font-size:0.82rem; color:var(--muted) }
.node.primary{ border-color:var(--accent); background:#fff; }

@media (max-width:900px){
  .node{ min-width:160px }
  .tree li{ padding:18px 10px 0 }
}
  </style>
</head>
<body>
  <div class="page">
    <header>
      <div>
        <h1>Struktur Kelas IX-B </h1>
        <div class="sub">Tahun Pelajaran 2025/2026</div>
      </div>
  <div class="tree">
    <ul>
      <li>
        <div class="node primary">
          <div class="role">Kelas</div>
          <div class="name">IX‑B</div>
        </div>
        <ul>
          <li>
            <div class="node">
              <div class="role">Wali Kelas</div>
              <div class="name">Musringatun,S.Pd.I</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Ketua Kelas</div>
              <div class="name">Ahmad Putra Nurrohim</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Wakil Ketua</div>
              <div class="name">Zaky Sofyan</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Sekretaris 1</div>
              <div class="name">Amelia Nur Rahmadani</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Sekretaris 2</div>
              <div class="name">Adelia Ainun Zakia</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Bendahara 1</div>
              <div class="name">Dewi Audray Agdiningviar</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Bendahara 2</div>
              <div class="name">Devi Nur Maulidda</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Seksi Kerohanian</div>
              <div class="name">1. Nabila Azzahra<br>2. Dira Hadi Erwanto</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Seksi Kesehatan</div>
              <div class="name">1. Muhammad Rishad T.A<br>2. Riyo Ramadhani</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Seksi Kebersihan</div>
              <div class="name">1. Muhamad Farras A.H<br>2. Dafi Idriansyah</div>
            </div>
          </li>
          <li>
            <div class="node">
              <div class="role">Seksi Keamanan</div>
              <div class="name">1. Muhamad Azriel Ardianta<br>2. Yogik Aditiyono</div>
            </div>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</div>
  </div>  <script>
    const allDetails = () => Array.from(document.querySelectorAll('details.group'));
    document.getElementById('expandAll').addEventListener('click', () => {
      allDetails().forEach(d => d.open = true);
    });
    document.getElementById('collapseAll').addEventListener('click', () => {
      allDetails().forEach(d => d.open = false);
    });
    document.getElementById('printBtn').addEventListener('click', () => window.print());
      `,
      anggota: `
       <head>
  <meta charset="UTF-8">
  <title>Daftar Siswa</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background:#fdfdfd;
      padding:1px;
    }
    table {
      border-collapse: collapse;
      width:110%;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 8px 12px;
      text-align: left;
    }
    th {
      background:#dfa86b;
      color:#fff;
    }
    .laki {
      background-color: #cce5ff; /* biru muda */
    }
    .perempuan {
      background-color: #ffd6e7; /* pink muda */
    }
  </style>
</head>
<body>
  <h2>Daftar Siswa Kelas IX-B</h2>
  <table>
    <tr>
      <th>No</th>
      <th>Nama</th>
    </tr>
    <tr class="perempuan"><td>1</td><td>Adelia Ainun Zakia</td></tr>
    <tr class="perempuan"><td>2</td><td>Adinda Selmi Yusfita</td></tr>
    <tr class="laki"><td>3</td><td>Ahmad Putra Nurrohim</td></tr>
    <tr class="perempuan"><td>4</td><td>Alisia Jastin</td></tr>
    <tr class="perempuan"><td>5</td><td>Amelia Nur Rahmadhani</td></tr>
    <tr class="perempuan"><td>6</td><td>Anita Sulfania</td></tr>
    <tr class="perempuan"><td>7</td><td>Cahya Nengrum Aulia Ulfah</td></tr>
    <tr class="perempuan"><td>8</td><td>Choliv Fuadiya</td></tr>
    <tr class="laki"><td>9</td><td>Dafi Idriansyah</td></tr>
    <tr class="perempuan"><td>10</td><td>Devi Nur Maulidda</td></tr>
        <tr class="perempuan"><td>11</td><td>Dewi Audray Agdiningviar</td></tr>
    <tr class="laki"><td>11</td><td>Dimas Surya Irawan</td></tr>
    <tr class="laki"><td>12</td><td>Dira Hadi Erwanto</td></tr>
    <tr class="perempuan"><td>13</td><td>Dwi Irji Febiana</td></tr>
    <tr class="laki"><td>14</td><td>Edo Hariyadi</td></tr>
    <tr class="laki"><td>15</td><td>Erwin Alvi Romdoni</td></tr>
    <tr class="laki"><td>16</td><td>Imana Pungky Mavavo</td></tr>
    <tr class="laki"><td>17</td><td>M. Rishad Tabatala Arshodiq</td></tr>
    <tr class="laki"><td>18</td><td>Micko Maulana</td></tr>
    <tr class="laki"><td>19</td><td>Muhamad Azriel Ardianta</td></tr>
    <tr class="laki"><td>20</td><td>Muhamad Farras Ahsanul Huda</td></tr>
    <tr class="laki"><td>21</td><td>Muhammad Arjuna Muarif Salam</td></tr>
    <tr class="laki"><td>22</td><td>Muhammad Fahmi Ferdiansyah</td></tr>
    <tr class="perempuan"><td>23</td><td>Mutiara Dwi Febrianti</td></tr>
    <tr class="perempuan"><td>24</td><td>Nabila Azzahra</td></tr>
    <tr class="perempuan"><td>25</td><td>Nur Sabrina</td></tr>
    <tr class="perempuan"><td>26</td><td>Putri Nur Ainiyyah Zahraa</td></tr>
    <tr class="laki"><td>27</td><td>Riyo Ramadhani</td></tr>
    <tr class="perempuan"><td>28</td><td>Silda Rimatus Zahro</td></tr>
    <tr class="perempuan"><td>29</td><td>Sintia Nabila</td></tr>
    <tr class="laki"><td>30</td><td>Yogik Aditiyono</td></tr>
    <tr class="laki"><td>31</td><td>Zaky Sofyan</td></tr>
  </table>
</body>
</html>
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
        <h1>Tugas / PR Terbaru Kamis,18 09 2025</h1>
        <ul>
          <h2>Loading...>
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
           <img src="hadiah1.jpg" style="width:100%; border-radius:10px;">
        <p>📷 foto bersama 😘
        <img src="hadiah2.jpg" style="width:100%; border-radius:10px;">
        <p>📷 foto bersama 😘
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
