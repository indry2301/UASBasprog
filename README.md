# UASBasprog
## Nama  : Indry Widiyani
## NIM   : 312210060
## Kelas : TI.22.C1
## Link Youtube: https://youtu.be/sLfhZtNCq9E
## Tutorial File PDF: [PROJEK UAS BAHASA PEMROGRAMAN.pdf](https://github.com/indry2301/UASBasprog/files/10419380/PROJEK.UAS.BAHASA.PEMROGRAMAN.pdf)

# Struktur Package & Modul
<img width="258" alt="package_model view" src="https://user-images.githubusercontent.com/115906333/211852419-85c7bb5c-0212-4e53-862b-398d41198c54.png">

# Penjelasan Program
## Model (daftar_nilai)
- Tambah Data
  - data = {} untuk menampung list data yang nanti akan terinput.
  - deklarasikan fungsi def tambah_data():
  - nama = input("Masukan nama: ") lalu tambahkan input nama, nim, nilai tugas, uts, uas.
  - nilai_akhir = (nilai_tugas)*30/100 + (nilai_uts)*35/100 + (nilai_uas)*35/100 untuk nilai akhir yang diambil dari perhitungan 3 komponen nilai (nilai_tugas: 30%, nilai_uts: 35%, nilai_uas: 35%).
  - data[nama] = [nama, nim, nilai_tugas, nilai_uts, nilai_uas, nilai_akhir] kita akan masukkan data yang tadi kita input ke dalam `data[nama]'.
  - lalu cetak print().
- Ubah Data
  - deklarasikan fungsi def ubah_data(): nama = input("Masukan nama untuk mengubah data: ") kita akan menginput data yang nanti akan di ubah.
  - if nama in data.keys(): print("Mau mengubah apa?") jika 'nama' dari di dalam 'data' maka akan mengembalikan daftar menggunakan fungsi 'keys()' lalu di cetak lah 'print()'.
  - sub_data = input("(Semua), (Nama), (NIM), (Tugas), (UTS), (UAS) : ") membuat menu ubah di dalam sub_data.
  - if sub_data.lower() == "semua": ambil kata kunci 'semua' di dalam sub_data jika 'semua' maka input data[nama][1] = input("Ubah NIM:") data[nama][2] = int(input("Ubah Nilai Tugas: ")) data[nama][3] = int(input("Ubah Nilai UTS: ")) data[nama][4] = int(input("Ubah Nilai UAS: ")).
  - data[nama][5] = data[nama][2] *30/100 + data[nama][3]*35/100 + data[nama][4] *35/100 kita dapatkan nilai akhir dengan diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%), ket: [5] = nilai_akhir, dimana [0] = nama.
  - lalu cetak print("\nBerhasil ubah data!").
  - Jika kita ingin mengubah data tertentu maka elif sub_data.lower() == "nim": data[nama][1] = input("NIM:") dan berlaku juga untuk nilai tugas, UTS dan UAS.
  - lalu cetak print("\nBerhasil ubah data!").
  - else: print("'{}' tidak ditemukan.".format(nama)) jika kita salah dalam memasukkan nama untuk mengubah data maka akan muncul 'nama tidak di temukan'.
- Cari Data
  - deklarasikan fungsi def cari_data():
  - nama = input("Masukan nama untuk mencari data: ") kita akan menginput data yang nanti akan dicari.
  - if nama in data.keys(): kita akan mengambil list 'nama' di dalam 'data' menggunakan pengkondisian.
  - maka cetak print("| {0:14} | {1:9} | {2:5} | {3:5} | {4:5} | {5:5}" .format(nama, data[nama][1], data[nama][2], data[nama][3], data[nama][4], data[nama][5])) untuk menampilkan data yang tersedia.
  - else: print("'{}' tidak ditemukan.".format(nama)) jika data yang kita input salah/tidak ditemukan maka akan tercetak 'nama tidak di temukan' -Hapus data.
  - deklarasikan fungsi def hapus_data():
  - nama = input("Masukan nama untuk menghapus data : ") kita akan menginput data yang nanti akan dihapus.
  - if nama in data.keys(): kita mengambil list 'nama' di dalam 'data' menggunakan pengkondisian.
  - del data[nama] hapus semua 'nama' yang ada di dalam 'data'.
  - jika sudah maka cetak print("sub_data '{}' berhasil dihapus.".format(nama)).
  - else: print("'{}' tidak ditemukan.".format(nama)) jika ada data yang kita input salah/tidak ditemukan maka akan di tercetak 'nama tidak ditemukan'.
## View (input_nilai)
- menambahkan fungsi input yang nantinya akan di deklarasikan di setiap modulenya, def input_nama(): def input_nim(): dan yang lainnya, yang nanti akan di masukkan kedalam data={}.
## View (view_nilai)
- deklarasikan fungsi def lihat_data(): kita menggunakan kondisi percabangan if, ambil data dari data.
- lalu cetak print().
## Code Main
![code](https://user-images.githubusercontent.com/115906333/212092109-90b74e5a-4608-4598-800c-0f81d1d7ea18.png)

# Output Program
## Tampilan Awal
<img width="580" alt="tampilan_awal" src="https://user-images.githubusercontent.com/115906333/212092998-ab12759c-c788-4280-bc8e-df487e95147b.png">

## Tampilan Tambah Data
- Disini saya akan menambahkan 3 data mahasiswa

<img width="589" alt="menu_tambah(1)" src="https://user-images.githubusercontent.com/115906333/212093152-2b3ce1f5-5737-48e7-a644-8772f466b148.png">

<img width="560" alt="menu_tambah(2)" src="https://user-images.githubusercontent.com/115906333/212093232-2706bd6b-3579-4d25-b785-09dc206dde9a.png">

## Menu Lihat Setelah Ditambahkan Data
- Terlihat ada 3 data mahasiswa yang selesai ditambahkan.

<img width="563" alt="menu_lihat(setelahtambah)" src="https://user-images.githubusercontent.com/115906333/212093447-a403c3e6-6a18-4622-9d64-9433187d7fb5.png">

## Tampilan Ubah Data
- Masukkan data nama mahasiswa yang ingin diubah datanya, dan nilai mana yang akan diubah.
- Disini saya akan mengubah nilai UAS menjadi 82 sedangkan nilai sebelumnya yaitu 75.

<img width="565" alt="menu_ubah" src="https://user-images.githubusercontent.com/115906333/212093664-5dfe8ca0-e292-4470-890f-1e80b62962b5.png">

## Menu Lihat Setelah Data Diubah
- Terlihat bahwa data nilai UAS widi sudah berubah.

<img width="564" alt="menu_lihat(setelahubah)" src="https://user-images.githubusercontent.com/115906333/212093978-b82a5e6f-aacb-4fa9-af07-4bc6bf759ecd.png">

## Tampilan Cari Data
- Masukkan nama untuk mencari data.
- Disini saya mencari data dengan nama widi.

<img width="566" alt="menu_cari" src="https://user-images.githubusercontent.com/115906333/212094087-2ff9ee34-b78d-4e8a-be65-976c6536f446.png">

## Tampilan Hapus Data
- Masukkan nama yang ingin dihapus datanya.
- Disini saya menghapus data yani.

<img width="570" alt="menu_hapus" src="https://user-images.githubusercontent.com/115906333/212094293-decf50ef-04f9-4977-b543-331386657776.png">

## Menu Lihat Setelah Data Dihapus
- Dan dibawah ini tampilan menu lihat setelah data atas nama yani dihapus.

<img width="558" alt="menu_lihat(setelahhapus)" src="https://user-images.githubusercontent.com/115906333/212094593-4df06acd-5f01-48f7-a8d7-d23f4753f006.png">

## Tampilan Keluar

<img width="564" alt="menu_keluar" src="https://user-images.githubusercontent.com/115906333/212094416-193dd4a1-4194-4c80-9388-090fc990c788.png">

# Cukup sekian dan terimakasih, semoga bermanfaat.









