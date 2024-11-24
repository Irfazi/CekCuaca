# CekCuaca
 Tugas 6 - 2210010277

CekCuaca adalah aplikasi berbasis Java yang memungkinkan pengguna untuk mendapatkan informasi cuaca terkini berdasarkan nama kota. Program ini memanfaatkan **OpenWeatherMap API** untuk mengambil data cuaca secara real-time.

## Fitur
- Masukkan nama kota untuk mendapatkan informasi cuaca saat ini.
- Data yang diperoleh mencakup:
  - Nama kota
  - Suhu (dalam Celcius)
  - Kondisi cuaca (cerah, hujan, dll.)
  - Kecepatan angin

## Persyaratan
- Java Development Kit (JDK) 8 atau versi yang lebih baru.
- Koneksi internet untuk mengakses API cuaca.

## Instalasi dan Penggunaan
1. Clone atau unduh repository ini.
2. Pastikan Anda memiliki file `CekCuaca.java` di dalam direktori project Anda.
3. Daftarkan akun di [OpenWeatherMap](https://openweathermap.org/) untuk mendapatkan **API Key**.
4. Masukkan API Key Anda pada kode program di bagian berikut:
   ```java
   private static final String API_KEY = "API_KEY_ANDA";
   ```
5. Kompilasi program dengan perintah:
   ```bash
   javac CekCuaca.java
   ```
6. Jalankan program dengan perintah:
   ```bash
   java CekCuaca
   ```

# Pengelolaan Kontak

Aplikasi ini adalah implementasi manajemen kontak sederhana berbasis GUI menggunakan Java `JFrame` dan SQLite untuk penyimpanan data.



## Teknologi

- **Bahasa Pemrograman**: Java
- **Database**: SQLite
- **GUI**: JFrame

## Contoh Kode

Berikut adalah salah satu bagian kode GUI yang digunakan dalam aplikasi:

### **Kode Tombol Tambah Kontak**

```java
// Membuat tombol tambah kontak
JButton btnTambah = new JButton("Tambah");
btnTambah.addActionListener(e -> {
    // Aksi yang dilakukan saat tombol diklik
    String nama = textFieldNama.getText();
    String telepon = textFieldTelepon.getText();
    // Masukkan data ke database menggunakan PengelolaanKontakHelper
    pengelolaanKontakHelper.tambahKontak(nama, telepon);
    JOptionPane.showMessageDialog(null, "Kontak berhasil ditambahkan!");
});
panel.add(btnTambah);
```

### **Kode Tombol Hapus Kontak**

```java
// Membuat tombol hapus kontak
JButton btnHapus = new JButton("Hapus");
btnHapus.addActionListener(e -> {
    // Aksi yang dilakukan saat tombol diklik
    String nama = textFieldNama.getText();
    pengelolaanKontakHelper.hapusKontak(nama);
    JOptionPane.showMessageDialog(null, "Kontak berhasil dihapus!");
});
panel.add(btnHapus);
```

## Catatan
- Jika program tidak dapat menemukan kota yang dimasukkan, pastikan nama kota sesuai dengan format yang didukung oleh OpenWeatherMap API.
- Pastikan API Key Anda valid dan memiliki akses ke layanan cuaca.

## Lisensi
Proyek ini dilisensikan di bawah MIT License.
