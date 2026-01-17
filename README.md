
           DOKUMENTASI RESMI SISTEM MANAJEMEN SERVIS GADGET
                    ASDPro - TJ PHONE REPAIR GALLERY 
                          VERSION 2.5.4 (2026)


Terima kasih telah memilih ASDPro sebagai solusi manajemen operasional
bisnis reparasi gadget Anda. Dokumen ini berisi panduan instalasi, 
konfigurasi sistem, keamanan data, hingga troubleshooting tingkat lanjut.

Harap baca dokumen ini secara menyeluruh untuk memastikan sistem berjalan
secara optimal dan data pelanggan Anda tetap aman.

---------------------------------------------------------------------------
DAFTAR ISI
---------------------------------------------------------------------------
1. PENGENALAN SISTEM (FILOSOFI & TUJUAN)
2. SPESIFIKASI MINIMUM HARDWARE & SOFTWARE
3. PROSEDUR INSTALASI YANG AMAN (BEST PRACTICE)
4. STRUKTUR SISTEM DAN PENYAMARAN FILE (KEAMANAN)
5. MANAJEMEN DATABASE & STRATEGI BACKUP (VITAL)
6. INTEGRASI HARDWARE (PRINTER THERMAL & SCANNER)
7. PENANGANAN MASALAH (TROUBLESHOOTING)
8. KEBIJAKAN PEMBARUAN (UPDATE POLICY)
9. KONTAK DUKUNGAN TEKNIS (SUPPORT)

---------------------------------------------------------------------------
PENGENALAN SISTEM
---------------------------------------------------------------------------
ASDPro (TJ Phone Repair Gallery) dirancang khusus untuk memenuhi kebutuhan
teknisi gadget modern. Sistem ini mengintegrasikan pencatatan nota masuk, 
pelacakan status pengerjaan, penyimpanan data, hingga pencetakkan nota
dalam satu platform yang ringan dan cepat.

Sistem ini dibangun menggunakan arsitektur Python yang telah dikompilasi 
ke dalam bahasa mesin (Binary) menggunakan Nuitka, memberikan performa 
maksimal dan keamanan kode dari upaya reverse-engineering pihak ketiga.

---------------------------------------------------------------------------
SPESIFIKASI MINIMUM HARDWARE & SOFTWARE
---------------------------------------------------------------------------
Agar ASDPro berjalan dengan lancar tanpa lag, pastikan perangkat Anda
memenuhi kriteria berikut:

Hardware:
- Prosesor: Intel Core i3 (Generasi 4+) atau setara.
- RAM: Minimal 4GB (8GB sangat disarankan untuk multitasking).
- Penyimpanan: Minimal 500MB ruang kosong (SSD disarankan).
- Resolusi Layar: Minimal 1366x768 (Optimal di Full HD 1920x1080).

Software:
- Sistem Operasi: Windows 10 atau Windows 11 (64-bit).
- Arsitektur: x86_64.
- Hak Akses: Administrator (Wajib untuk penulisan log sistem).

---------------------------------------------------------------------------
PROSEDUR INSTALASI YANG AMAN
---------------------------------------------------------------------------
Langkah-langkah instalasi ASDPro-2026:

1. Pastikan tidak ada versi ASDPro lama yang sedang berjalan.
2. Klik kanan pada file 'ASDPro-2026.exe' dan pilih 'Run as Administrator'.
3. Jika muncul pesan "Windows Protected Your PC", klik "More Info" lalu 
   klik "Run Anyway". Hal ini wajar terjadi karena sistem menggunakan 
   metode enkripsi tingkat tinggi yang belum terdaftar secara digital di 
   Microsoft SmartScreen.
4. Ikuti instruksi di layar. Folder instalasi default adalah:
   C:\Program Files\TJ Phone Repair Gallery
5. Setelah instalasi selesai, sistem akan membuat shortcut di Desktop 
   dengan nama "TJ Phone Repair Gallery".

---------------------------------------------------------------------------
STRUKTUR SISTEM DAN PENYAMARAN FILE
---------------------------------------------------------------------------
Untuk alasan keamanan dan integritas sistem dari serangan virus, ASDPro 
menggunakan struktur file yang tidak standar di dalam folder instalasi:

- srv_host_core.exe: Merupakan file eksekusi utama (Main Engine). 
  File ini disamarkan agar tidak mudah dikenali oleh software berbahaya.
- sys_kernel.dll & api_bridge.inf: Library pendukung yang mengontrol 
  komunikasi antara database dan tampilan UI. Jangan menghapus file ini.
- Folder SystemX: Folder terenkripsi tempat mesin utama berada.

PERINGATAN: Modifikasi manual pada file di dalam folder instalasi dapat 
menyebabkan sistem "Corrupt" dan kegagalan fungsi cetak nota.

---------------------------------------------------------------------------
MANAJEMEN DATABASE & STRATEGI BACKUP
---------------------------------------------------------------------------
Keamanan data nota pelanggan adalah prioritas utama kami. Berbeda dengan 
aplikasi biasa, ASDPro memisahkan file sistem dan file data.

Lokasi Database:
C:\ProgramData\TJPhoneRepair\service_data.db

PENTING:
- Folder ProgramData adalah folder tersembunyi (Hidden Folder).
- Saat Anda melakukan Uninstall aplikasi, file 'service_data.db' TIDAK 
  AKAN dihapus. Ini fitur keamanan agar data Anda tidak hilang jika Anda 
  hanya ingin melakukan update versi.

Strategi Backup (Sangat Disarankan):
Kami menyarankan Anda menyalin file 'service_data.db' ke Cloud (Google 
Drive/Dropbox) atau Flashdisk secara rutin setiap tutup toko (pukul 21.00).

---------------------------------------------------------------------------
INTEGRASI HARDWARE (PRINTER THERMAL & SCANNER)
---------------------------------------------------------------------------
ASDPro mendukung mayoritas printer thermal 58mm dan 80mm:
1. Pastikan driver printer thermal sudah terpasang di Windows.
2. Atur printer tersebut sebagai 'Default Printer' di Control Panel.
3. ASDPro akan otomatis mendeteksi lebar kertas dan menyesuaikan layout 
   nota secara proporsional.

Untuk penggunaan Barcode Scanner, sistem mendukung mode 'Plug and Play' 
melalui koneksi USB HID. Pastikan kursor berada pada kolom 'Input IMEI/SN' 
sebelum melakukan scanning.

---------------------------------------------------------------------------
PENANGANAN MASALAH (TROUBLESHOOTING)
---------------------------------------------------------------------------
Q: Aplikasi tidak mau terbuka saat diklik?
A: Pastikan antivirus tidak mengkarantina file 'srv_host_core.exe'. 
   Tambahkan folder instalasi ke dalam 'Exclusion List' di antivirus Anda.

Q: Nota tidak mau tercetak?
A: Periksa antrean print (Spooler) di Windows. Pastikan status printer 
   adalah 'Online' dan kertas masih tersedia.

Q: Data nota hari ini hilang?
A: Periksa apakah Anda tidak sengaja memindahkan file 'service_data.db' 
   dari folder ProgramData. Pastikan izin tulis (write permission) aktif.

---------------------------------------------------------------------------
KEBIJAKAN PEMBARUAN (UPDATE POLICY)
---------------------------------------------------------------------------
Update ASDPro dirilis secara berkala untuk menambal celah keamanan dan 
menambah fitur baru. 
- Sebelum melakukan update, selalu backup database Anda.
- Jalankan installer versi terbaru di atas versi lama tanpa menghapus 
  (Uninstall) terlebih dahulu. Installer akan secara otomatis menimpa 
  file sistem lama dengan yang baru.

---------------------------------------------------------------------------
KONTAK DUKUNGAN TEKNIS
---------------------------------------------------------------------------
Jika Anda mengalami kesulitan teknis yang tidak dapat diatasi melalui 
panduan ini, silakan hubungi tim pengembang kami:

Pengembang: ASDPro Tech
Lead Dev  : [ASDPro Tech Support]
WhatsApp  : [+62812-71020270]
Email     : [tjphonerepair@gmail.com]
Website   : [www.tjphonerepair.id]

(c) 2026 TJ Phone Repair Gallery. All Rights Reserved.
Dibuat dengan dedikasi untuk kemajuan teknisi Indonesia.
===========================================================================
