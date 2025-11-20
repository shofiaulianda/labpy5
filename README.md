## Nama : Shofi Aulianda
## NIM : 312510183
## Kelas : TI.25.A.2
## Pertemuan : 10
## Mata Kuliah : Pengantar Pemrograman 

## Kode Latihan
<img width="539" height="409" alt="Screenshot_20251120_114925" src="https://github.com/user-attachments/assets/6848fa68-4e29-43f3-a220-7f14fb0ae51e" />

## Output Latihan 
<img width="755" height="193" alt="Screenshot_20251120_124937" src="https://github.com/user-attachments/assets/9794981b-8ab4-4516-986e-60a8d7109474" />

## Kode Praktikum
<img width="577" height="407" alt="Screenshot_20251120_114453" src="https://github.com/user-attachments/assets/d1ee7904-548d-448d-83bf-91edf7ecf0bb" />

## Output Praktikum
<img width="767" height="217" alt="Screenshot_20251120_125147" src="https://github.com/user-attachments/assets/3623ab03-c1c0-4fd1-8e46-3e378321d27b" />

## Flowchart
```
                   ┌────────────────────────┐
                   │     MULAI PROGRAM      │
                   └───────────┬────────────┘
                               │
                               ▼
                   ┌────────────────────────┐
                   │   TAMPILKAN MENU        │
                   └───────────┬────────────┘
                               │
                               ▼
                   ┌────────────────────────┐
                   │   INPUT PILIHAN MENU    │
                   └───────────┬────────────┘
             ┌─────────────────┼──────────────────┐
             ▼                 ▼                  ▼

   ┌────────────────┐   ┌────────────────┐   ┌──────────────────────┐
   │ Pilihan = 1 ?   │   │ Pilihan = 2 ?   │   │ Pilihan = 3 ?         │
   └───────┬────────┘   └───────┬────────┘   └───────────┬──────────┘
           │                    │                       │
           ▼                    ▼                       ▼

┌─────────────────────┐  ┌──────────────────────┐ ┌───────────────────────┐
│ INPUT nama, nim,     │  │ INPUT nama yang akan │ │ INPUT nama yang akan   │
│ tugas, uts, uas      │  │ diubah               │ │ dihapus                │
│ HITUNG nilai akhir   │  │ Jika ada → ubah data │ │ Jika ada → hapus data  │
│ SIMPAN ke dictionary │  │ Jika tidak → pesan   │ │ Jika tidak → pesan     │
└─────────┬───────────┘  └───────────┬──────────┘ └────────────┬──────────┘
          │                         │                         │
          └──────────────┬──────────┴───────────────┬─────────┘
                         │                          │
                         ▼                          ▼

              ┌──────────────────────┐     ┌───────────────────────┐
              │   Pilihan = 4 ?       │     │    Pilihan = 5 ?       │
              └───────────┬──────────┘     └───────────┬───────────┘
                          │                            │
                          ▼                            ▼
      ┌────────────────────────────┐   ┌─────────────────────────────┐
      │ TAMPILKAN semua data       │   │ INPUT nama yang dicari       │
      │ Jika kosong → pesan        │   │ Jika ada → tampilkan         │
      └──────────┬─────────────────┘   │ Jika tidak → pesan           │
                 │                     └──────────┬──────────────────┘
                 │                                │
                 └───────────────┬────────────────┘
                                 │
                                 ▼
                     ┌───────────────────────┐
                     │   Pilihan = 0 ?        │
                     └────────────┬───────────┘
                                  │
                                  ▼
                        ┌────────────────────┐
                        │    KELUAR PROGRAM   │
                        └────────────────────┘

```
## Penjelasan Program
1. Dictionary Data Mahasiswa

data_mahasiswa = {}

Semua data mahasiswa akan disimpan dalam dictionary dengan format:
```
data_mahasiswa[nama] = {

    "tugas": nilai,

    "uts": nilai,

    "uas": nilai,

    "akhir": nilai_akhir

}
```
2. Fungsi hitung_nilai_akhir()
```
def hitung_nilai_akhir(tugas, uts, uas):
    return (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
``

Fungsi ini menghitung nilai akhir berdasarkan bobot:

*Tugas : 30%

*UTS : 35%

*UAS : 35%

 3. Menu Utama (Looping while True)

Program menampilkan menu dan meminta pengguna memilih salah satu:
```
1. Tambah Data
2. Ubah Data
3. Hapus Data
4. Tampilkan Data
5. Cari Data
0. Keluar
```
Proses berlangsung terus sampai pengguna memilih 0.

 4. Tambah Data (Menu 1)

Program meminta input:

*nama

*nim

*nilai tugas

*nilai UTS

*nilai UAS

Lalu menghitung nilai akhir, kemudian menyimpan data ke dictionary.

 5. Ubah Data (Menu 2)

Pengguna memasukkan nama mahasiswa yang akan diubah.

Jika ditemukan, data diperbarui dengan input nilai baru.

Jika tidak ditemukan → tampil pesan "Data tidak ditemukan!"

 6. Hapus Data (Menu 3)

Pengguna memasukkan nama mahasiswa yang ingin dihapus.

Jika ada → data dihapus.

Jika tidak → muncul pesan.

7. Tampilkan Semua Data (Menu 4)

Menampilkan semua mahasiswa dalam dictionary.

Jika data kosong → tampil "Belum ada data."

 8. Cari Data (Menu 5)

Pengguna memasukkan nama.
Jika ada, tampil data mahasiswa.

 BUG yang muncul
Pada saat menampilkan NIM, kamu menggunakan nim dari variabel terakhir, karena NIM tidak disimpan.

 9. Keluar (Menu 0)

Mengakhiri program.
