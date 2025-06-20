<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Formulir Pelatihan Scuba Dasar - SSDC</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary: #005792;
      --secondary: #00a8e8;
      --accent: #0077b6;
      --light: #f0f8ff;
      --dark: #003366;
      --success: #28a745;
      --warning: #ffc107;
      --danger: #dc3545;
      --ocean-blue: #006994;
      --sea-green: #008080;
    }

    body {
      font-family: 'Poppins', sans-serif;
      line-height: 1.6;
      background: linear-gradient(135deg, #e0f7fa, #f0f8ff);
      color: #333;
      padding: 20px;
      min-height: 100vh;
      position: relative;
      overflow-x: hidden;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
      position: relative;
    }

    header {
      text-align: center;
      padding: 30px 0 25px;
      margin-bottom: 30px;
      position: relative;
      overflow: hidden;
      border-radius: 12px;
      background: white;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
    }

    header::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 6px;
      background: linear-gradient(90deg, var(--accent), var(--secondary), var(--primary));
    }

    header h1 {
      font-size: 2.2rem;
      margin: 15px 0 10px;
      letter-spacing: 0.5px;
      color: var(--primary);
      font-weight: 600;
    }

    header p {
      font-size: 1.1rem;
      max-width: 800px;
      margin: 0 auto;
      color: #555;
      padding: 0 20px;
    }

    .logo {
      width: 180px;
      height: auto;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .logo img {
      width: 100%;
      height: auto;
      max-height: 140px;
      object-fit: contain;
      transition: transform 0.3s ease;
    }

    .logo img:hover {
      transform: scale(1.05);
    }

    .main-content {
      background: white;
      border-radius: 12px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
      padding: 30px;
      margin-bottom: 30px;
      border: 1px solid rgba(0,0,0,0.05);
    }

    .section-title {
      color: var(--primary);
      margin-bottom: 25px;
      padding-bottom: 12px;
      border-bottom: 3px solid var(--accent);
      font-size: 1.7rem;
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 600;
    }

    .section-title i {
      color: var(--secondary);
      background: rgba(0,119,182,0.1);
      padding: 10px;
      border-radius: 50%;
    }

    .form-group {
      margin-bottom: 25px;
    }

    label {
      display: block;
      margin-bottom: 8px;
      font-weight: 500;
      color: var(--dark);
      font-size: 1.05rem;
    }

    .required::after {
      content: " *";
      color: var(--danger);
    }

    input, select, textarea {
      width: 100%;
      padding: 14px;
      border: 2px solid #e0e0e0;
      border-radius: 10px;
      font-size: 16px;
      transition: all 0.3s;
      background-color: #f9f9f9;
      font-family: 'Poppins', sans-serif;
    }

    input:focus, select:focus, textarea:focus {
      border-color: var(--accent);
      outline: none;
      box-shadow: 0 0 0 3px rgba(0, 119, 182, 0.15);
      background-color: white;
    }

    .radio-group {
      display: flex;
      gap: 20px;
      margin-top: 10px;
      flex-wrap: wrap;
    }

    .radio-option {
      display: flex;
      align-items: center;
      gap: 8px;
      flex: 1;
      min-width: 120px;
    }

    .radio-option input[type="radio"] {
      width: auto;
      margin-right: 5px;
    }

    .program-info {
      background-color: #e3f2fd;
      padding: 25px;
      border-radius: 10px;
      margin: 35px 0;
      border-left: 5px solid var(--secondary);
    }

    .program-info h3 {
      color: var(--primary);
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 1.4rem;
    }

    .program-info p {
      margin-bottom: 12px;
      font-size: 1rem;
      color: #333;
    }

    .price-highlight {
      font-size: 1.15rem;
      font-weight: bold;
      color: var(--success);
      background: rgba(40, 167, 69, 0.1);
      padding: 6px 12px;
      border-radius: 6px;
      display: inline-block;
      margin-top: 8px;
    }

    /* Responsive table styles */
    .table-container {
      margin-top: 25px;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
      border: 1px solid #e0e0e0;
    }

    .course-table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.95rem;
    }

    .course-table th {
      background-color: var(--primary);
      color: white;
      padding: 14px 16px;
      text-align: left;
      font-weight: 500;
    }

    .course-table td {
      padding: 14px 16px;
      border: 1px solid #e9ecef;
    }

    .course-table tr:nth-child(even) {
      background-color: #f8f9fa;
    }

    .course-table tr:hover {
      background-color: #e3f2fd;
    }

    /* Stacked table for mobile */
    @media (max-width: 600px) {
      .course-table {
        min-width: auto;
      }
      
      .course-table, .course-table thead, .course-table tbody, 
      .course-table th, .course-table td, .course-table tr {
        display: block;
      }
      
      .course-table thead tr {
        position: absolute;
        top: -9999px;
        left: -9999px;
      }
      
      .course-table tr {
        border: 1px solid #dee2e6;
        margin-bottom: 20px;
        border-radius: 10px;
        overflow: hidden;
      }
      
      .course-table td {
        border: none;
        border-bottom: 1px solid #e9ecef;
        position: relative;
        padding-left: 50%;
        padding-top: 14px;
        padding-bottom: 14px;
      }
      
      .course-table td:before {
        position: absolute;
        top: 14px;
        left: 15px;
        width: 40%;
        padding-right: 15px;
        white-space: nowrap;
        font-weight: 600;
        color: var(--primary);
      }
      
      .course-table td:nth-of-type(1):before { content: "Program"; }
      .course-table td:nth-of-type(2):before { content: "Lokasi"; }
      .course-table td:nth-of-type(3):before { content: "Total Biaya"; }
    }

    .btn-submit {
      background: linear-gradient(135deg, var(--primary), var(--accent));
      color: white;
      border: none;
      padding: 16px 30px;
      font-size: 18px;
      font-weight: 600;
      border-radius: 10px;
      cursor: pointer;
      width: 100%;
      transition: all 0.3s;
      letter-spacing: 0.5px;
      margin-top: 25px;
      display: block;
      max-width: 380px;
      margin-left: auto;
      margin-right: auto;
      position: relative;
      overflow: hidden;
      z-index: 1;
      box-shadow: 0 4px 12px rgba(0, 87, 146, 0.25);
    }

    .btn-submit::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 0%;
      height: 100%;
      background: linear-gradient(135deg, var(--accent), var(--primary));
      transition: all 0.4s;
      z-index: -1;
    }

    .btn-submit:hover::before {
      width: 100%;
    }

    .btn-submit:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 18px rgba(0, 87, 146, 0.35);
    }

    .btn-submit:disabled {
      background: #a0a0a0;
      cursor: not-allowed;
      transform: none;
      box-shadow: none;
    }

    .btn-submit:disabled::before {
      width: 0%;
    }

    .materials-list {
      list-style-type: none;
      margin: 30px 0;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 15px;
    }

    .materials-list li {
      padding: 16px 18px;
      background-color: #e3f2fd;
      border-left: 4px solid var(--accent);
      border-radius: 0 8px 8px 0;
      display: flex;
      align-items: center;
      gap: 15px;
      font-size: 1rem;
      transition: all 0.3s;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    .materials-list li:hover {
      transform: translateY(-3px);
      box-shadow: 0 4px 10px rgba(0,0,0,0.08);
    }

    .materials-list li i {
      color: var(--secondary);
      font-size: 1.3rem;
      min-width: 30px;
    }

    .disclaimer {
      background-color: #fff8e1;
      padding: 22px;
      border-radius: 10px;
      margin: 35px 0;
      border-left: 5px solid var(--warning);
      font-size: 1rem;
    }

    .disclaimer h3 {
      color: var(--warning);
      margin-bottom: 15px;
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 1.4rem;
    }

    .contact-info {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      margin-top: 40px;
    }

    .contact-card {
      background: white;
      padding: 22px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.07);
      text-align: center;
      transition: transform 0.3s;
      font-size: 1rem;
      border: 1px solid #e9ecef;
      background: linear-gradient(to bottom, white, #f8fbff);
    }

    .contact-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
    }

    .contact-card i {
      font-size: 2.3rem;
      color: var(--secondary);
      margin-bottom: 18px;
      background: rgba(0,119,182,0.1);
      width: 65px;
      height: 65px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      margin: 0 auto 18px;
    }

    .contact-card h3 {
      color: var(--primary);
      margin-bottom: 12px;
      font-size: 1.25rem;
      font-weight: 600;
    }

    .contact-card p {
      color: #555;
      font-size: 1.05rem;
    }

    footer {
      text-align: center;
      padding: 25px 0;
      margin-top: 30px;
      color: var(--dark);
      border-top: 1px solid #e0e0e0;
      font-size: 0.95rem;
      background: rgba(255,255,255,0.9);
      border-radius: 10px;
    }

    .section-divider {
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--accent), transparent);
      margin: 40px 0;
      border: none;
    }

    .notification {
      position: fixed;
      top: 25px;
      right: 25px;
      padding: 18px 25px;
      border-radius: 10px;
      color: white;
      font-weight: 500;
      z-index: 1000;
      opacity: 0;
      transform: translateX(100%);
      transition: all 0.4s ease;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
      max-width: 380px;
      display: flex;
      align-items: center;
      gap: 15px;
      font-size: 1.05rem;
    }

    .notification.show {
      opacity: 1;
      transform: translateX(0);
    }

    .notification.success {
      background: var(--success);
      border-left: 6px solid #218838;
    }

    .notification.error {
      background: var(--danger);
      border-left: 6px solid #bd2130;
    }

    .notification i {
      font-size: 1.8rem;
    }

    .notification .message {
      flex: 1;
      line-height: 1.5;
    }

    .diver-icon {
      position: absolute;
      bottom: 20px;
      right: 20px;
      font-size: 3rem;
      color: var(--accent);
      opacity: 0.08;
      z-index: -1;
    }

    @media (max-width: 768px) {
      .main-content {
        padding: 25px;
      }
      
      header h1 {
        font-size: 2rem;
      }
      
      .section-title {
        font-size: 1.6rem;
      }
      
      .materials-list {
        grid-template-columns: 1fr;
      }
      
      .contact-card {
        padding: 20px;
      }
    }

    @media (max-width: 600px) {
      body {
        padding: 15px;
      }
      
      header {
        padding: 25px 0 20px;
      }
      
      header h1 {
        font-size: 1.8rem;
      }
      
      header p {
        font-size: 1rem;
      }
      
      .logo {
        width: 150px;
      }
      
      .main-content {
        padding: 20px 15px;
      }
      
      .section-title {
        font-size: 1.5rem;
      }
      
      .radio-group {
        flex-direction: column;
        gap: 12px;
      }
      
      .radio-option {
        width: 100%;
      }
      
      .program-info {
        padding: 20px;
      }
      
      .btn-submit {
        padding: 15px;
        font-size: 17px;
        max-width: 100%;
      }
      
      .contact-info {
        grid-template-columns: 1fr;
        gap: 20px;
      }
      
      .notification {
        top: 15px;
        right: 15px;
        left: 15px;
        max-width: none;
        padding: 15px 20px;
      }
      
      .diver-icon {
        display: none;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">
        <img src="https://ssdc-samudera-scuba-diving-club.neocities.org/SSDC%20logo%20n.b.png" alt="SSDC Logo">
      </div>
      <h1>Formulir Pendaftaran Latihan SCUBA Dasar</h1>
      <p>Selamat datang di SSDC (Samudra Scuba Diving Club) - Langkah pertama Anda dalam petualangan bawah air</p>
    </header>
    
    <div class="main-content">
      <h2 class="section-title"><i class="fas fa-user"></i> Data Peserta</h2>
      
      <form id="scubaForm">
        <div class="form-group">
          <label for="nama" class="required">Nama Lengkap</label>
          <input type="text" id="nama" name="nama" placeholder="Masukkan nama lengkap" required>
        </div>
        
        <div class="form-group">
          <label for="ttl" class="required">Tanggal Lahir</label>
          <input type="date" id="ttl" name="ttl" required>
        </div>
        
        <div class="form-group">
          <label class="required">Jenis Kelamin</label>
          <div class="radio-group">
            <div class="radio-option">
              <input type="radio" id="male" name="gender" value="Laki-laki" required>
              <label for="male">Laki-laki</label>
            </div>
            <div class="radio-option">
              <input type="radio" id="female" name="gender" value="Perempuan">
              <label for="female">Perempuan</label>
            </div>
          </div>
        </div>
        
        <div class="form-group">
          <label for="telp" class="required">No. Telepon</label>
          <input type="tel" id="telp" name="telp" placeholder="Contoh: 081234567890" required>
        </div>
        
        <div class="form-group">
          <label for="email" class="required">Email</label>
          <input type="email" id="email" name="email" placeholder="email@contoh.com" required>
        </div>
        
        <div class="form-group">
          <label for="sertifikasi">Tingkat Sertifikasi (jika ada)</label>
          <input type="text" id="sertifikasi" name="sertifikasi" placeholder="Contoh: Open Water Diver">
        </div>
        
        <div class="form-group">
          <label for="no_sertifikat">No. Registrasi Sertifikat</label>
          <input type="text" id="no_sertifikat" name="no_sertifikat">
        </div>
        
        <div class="form-group">
          <label for="lokasi_sertifikat">Lokasi Sertifikasi</label>
          <input type="text" id="lokasi_sertifikat" name="lokasi_sertifikat" placeholder="Tempat sertifikasi sebelumnya">
        </div>
        
        <div class="form-group">
          <label for="tujuan" class="required">Tujuan Latihan</label>
          <select id="tujuan" name="tujuan" required>
            <option value="">-- Pilih Tujuan Latihan --</option>
            <option value="Sertifikasi">Sertifikasi</option>
            <option value="Discovery">Discovery (Pengenalan)</option>
            <option value="Refreshing">Refreshing (Penyegaran)</option>
          </select>
        </div>
        
        <div class="program-info">
          <h3><i class="fas fa-info-circle"></i> Informasi Program</h3>
          <p><strong>Durasi:</strong> 3 hari (Teori + Praktek)</p>
          <p><strong>Persyaratan:</strong> Sehat jasmani & rohani, usia minimal 12 tahun</p>
          <p><strong>Biaya:</strong> <span class="price-highlight">Tabel biaya program</span></p>
          
          <div class="table-container">
            <h4 style="color: var(--primary); margin: 15px 0 10px; font-size: 1.1rem;"><i class="fas fa-money-bill-wave"></i> Tabel Biaya Program</h4>
            <table class="course-table">
              <thead>
                <tr>
                  <th>Program</th>
                  <th>Lokasi</th>
                  <th>Total Biaya</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>Sertifikasi</td>
                  <td>Derawan</td>
                  <td>Rp 7.225.000</td>
                </tr>
                <tr>
                  <td>Sertifikasi</td>
                  <td>Tarakan</td>
                  <td>Rp 4.850.000</td>
                </tr>
                <tr>
                  <td>Discovery (Kolam)</td>
                  <td>-</td>
                  <td>Rp 700.000</td>
                </tr>
                <tr>
                  <td>Refreshing (Kolam)</td>
                  <td>-</td>
                  <td>Rp 435.000</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
        
        <button type="submit" class="btn-submit" id="submitBtn">Daftar Sekarang</button>
      </form>
      
      <hr class="section-divider">
      
      <h2 class="section-title"><i class="fas fa-book"></i> Materi Latihan</h2>
      <ul class="materials-list">
        <li><i class="fas fa-check-circle"></i> Pengertian & Pengenalan Alat Scuba</li>
        <li><i class="fas fa-check-circle"></i> Prosedur: Descend, Ascend, Equalisasi, Sinyal Tangan</li>
        <li><i class="fas fa-check-circle"></i> Buoyancy Control, Mask Clearing, Recovery, Remove & Replace</li>
        <li><i class="fas fa-check-circle"></i> Bahaya Hewan Laut & Penyakit Penyelaman</li>
        <li><i class="fas fa-check-circle"></i> Fisika Penyelaman & Teknik Bongkar Pasang Alat</li>
        <li><i class="fas fa-check-circle"></i> Teknik Penyelamatan Dasar & Tanggap Darurat</li>
      </ul>
      
      <div class="disclaimer">
        <h3><i class="fas fa-exclamation-triangle"></i> Penting!</h3>
        <p>Semua peserta wajib mengisi formulir medis sebelum pelatihan dimulai. Peserta dengan kondisi medis tertentu harus menyertakan surat keterangan sehat dari dokter.</p>
      </div>
      
      <h2 class="section-title"><i class="fas fa-address-card"></i> Informasi Kontak</h2>
      <div class="contact-info">
        <div class="contact-card">
          <i class="fas fa-phone"></i>
          <h3>Telepon</h3>
          <p>+62 822 5603 3500</p>
        </div>
        <div class="contact-card">
          <i class="fas fa-envelope"></i>
          <h3>Email</h3>
          <p>elia.samudra@gmail.com</p>
        </div>
        <div class="contact-card">
          <i class="fas fa-map-marker-alt"></i>
          <h3>Lokasi</h3>
          <p>Lenderai Suslimana, Tarakan, Kalimantan Utara</p>
        </div>
      </div>
    </div>
    
    <footer>
      <p>© 2023 SSDC (Samudra Scuba Diving Club) | All Rights Reserved</p>
      <p>Formulir Pendaftaran Latihan SCUBA Dasar</p>
    </footer>
  </div>

  <div id="notification" class="notification">
    <i class="fas fa-info-circle"></i>
    <div class="message"></div>
  </div>

  <div class="diver-icon">
    <i class="fas fa-swimmer"></i>
  </div>

  <!-- Tambahkan library EmailJS -->
  <script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
  
  <script>
    document.addEventListener('DOMContentLoaded', function() {
      // Inisialisasi EmailJS dengan public key
      emailjs.init('dSrFXKtyoYoC5W44H');
      
      // Set tanggal minimal untuk tanggal lahir (12 tahun ke atas)
      const today = new Date();
      const minDate = new Date();
      minDate.setFullYear(today.getFullYear() - 12);
      document.getElementById('ttl').max = minDate.toISOString().split('T')[0];
      
      const form = document.getElementById('scubaForm');
      const submitBtn = document.getElementById('submitBtn');
      const notification = document.getElementById('notification');
      const messageDiv = notification.querySelector('.message');
      
      form.addEventListener('submit', async function(e) {
        e.preventDefault();
        
        // Validasi form
        const nama = document.getElementById('nama').value;
        const tujuan = document.getElementById('tujuan').value;
        const ttl = document.getElementById('ttl').value;
        const email = document.getElementById('email').value;
        
        if(!nama || !tujuan || !ttl || !email) {
          showNotification('Mohon lengkapi semua field yang wajib diisi!', 'error');
          return;
        }
        
        // Validasi email
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!emailRegex.test(email)) {
          showNotification('Format email tidak valid!', 'error');
          return;
        }
        
        // Disable tombol submit
        submitBtn.disabled = true;
        submitBtn.textContent = 'Mengirim...';
        
        try {
          // Mengumpulkan data form
          const formData = new FormData(form);
          const data = Object.fromEntries(formData.entries());
          
          // Kirim data ke email menggunakan EmailJS
          await sendEmail(data);
          
          // Tampilkan notifikasi sukses
          showNotification('Pendaftaran berhasil dikirim! Tim SSDC akan segera menghubungi Anda.', 'success');
          
          // Reset form setelah 2 detik
          setTimeout(() => {
            form.reset();
            submitBtn.disabled = false;
            submitBtn.textContent = 'Daftar Sekarang';
          }, 2000);
        } catch (error) {
          // Tampilkan notifikasi error dengan detail
          let errorMessage = 'Terjadi kesalahan saat mengirim formulir. Silakan coba lagi.';
          
          if (error.status === 400) {
            errorMessage = 'Data tidak valid. Mohon periksa kembali isian formulir.';
          } else if (error.status === 429) {
            errorMessage = 'Terlalu banyak permintaan. Silakan coba beberapa saat lagi.';
          } else if (error.text) {
            errorMessage = `Error: ${error.text}`;
          }
          
          showNotification(errorMessage, 'error');
          console.error('Error detail:', error);
          
          // Aktifkan kembali tombol submit
          submitBtn.disabled = false;
          submitBtn.textContent = 'Daftar Sekarang';
        }
      });
      
      // Fungsi untuk menampilkan notifikasi
      function showNotification(message, type) {
        messageDiv.textContent = message;
        notification.className = `notification ${type} show`;
        
        // Atur ikon sesuai jenis notifikasi
        const icon = notification.querySelector('i');
        if (type === 'success') {
          icon.className = 'fas fa-check-circle';
        } else {
          icon.className = 'fas fa-exclamation-circle';
        }
        
        // Sembunyikan notifikasi setelah 5 detik
        setTimeout(() => {
          notification.className = 'notification';
        }, 5000);
      }
      
      // Fungsi untuk mengirim email menggunakan EmailJS
      async function sendEmail(data) {
        // Gunakan service ID dan template ID Anda
        const serviceID = 'Gmail-SSDC';
        const templateID = 'template_vmdy1t4';
        
        // Format data agar sesuai dengan template
        const templateParams = {
          to_email: 'elia.samudra@gmail.com',
          subject: `Pendaftaran Baru: ${data.nama}`,
          nama: data.nama,
          ttl: formatDate(data.ttl),
          gender: data.gender,
          telp: data.telp,
          email: data.email,
          sertifikasi: data.sertifikasi || 'Tidak ada',
          no_sertifikat: data.no_sertifikat || 'Tidak ada',
          lokasi_sertifikat: data.lokasi_sertifikat || 'Tidak ada',
          tujuan: data.tujuan,
          timestamp: new Date().toLocaleString('id-ID', {
            weekday: 'long',
            year: 'numeric',
            month: 'long',
            day: 'numeric',
            hour: '2-digit',
            minute: '2-digit'
          })
        };
        
        // Kirim email menggunakan EmailJS
        return emailjs.send(serviceID, templateID, templateParams);
      }
      
      // Fungsi untuk format tanggal
      function formatDate(dateString) {
        if (!dateString) return '';
        const date = new Date(dateString);
        return date.toLocaleDateString('id-ID', {
          weekday: 'long',
          year: 'numeric',
          month: 'long',
          day: 'numeric'
        });
      }
    });
  </script>
</body>
</html>
