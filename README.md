# Praktikum 7

Nama : Nurul Aisyah

NIM : 312310476

Kelas : TI.23.A.5

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Latihan|[Click Here](#latihan)|
|2|Praktikum6|[Click Here](#praktikum6)|
|3|Flowchart Praktikum6|[Click Here](#flowchart-praktikum-6)|

## Latihan
Ubahlah kode di bawah ini menjadi fungsi menggunakan lambda
   
    import math

    def a(x):
    return x**2

    def b(x, y):
    return math.sqrt(x**2 + y**2)

    def c(*args):
    return sum(args)/len(args)

    def d(s):
    return "".join(set(s))
    
### Rumus :
    # Latihan

    print("Nama : Nurul Aisyah")
    print("NIM  : 312310476")
    print("=========================")

    import math
    def a(x):
        return x**2
        a = lambda x: x**2, a
    print(a(2))

    def b(x, y):
        return math.sqrt(x**2 + y**2)
        b = lambda x, y: x**2 + y**2, b
    print(b(2, 4))

    def c(*args):
        return sum(args) / len(args)
        c = lambda*args: sum(args) / len(args)
    print(c(10, 50))

    def d(s):
        return "".join(set(s))
        d = lambda s: "".join(set(s))
    print(d("Nurul"))
    
### Program :
![alt text](?raw=true)
### Hasil Run :

![alt text](?raw=true)

## Praktikum 6
Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan :

- Fungsi tambah() untuk menambah data.
- Fungsi tampilkan() untuk menampilkan data.
- Fungsi hapus(nama) untuk menghapus data berdasarkan nama.
- Fungsi ubah(nama) untuk mengubah data berdasarkan nama.
- Buat Flowchart dan Penjelasan Programnya pada README.md.
-  Commit dan push repository ke github.

### Rumus :
    from os import system
    s_nama = []
    s_nim = []
    s_tugas = []
    s_uts = []
    s_uas = []
    s_akhir = []


    def judul():
        print('==================================')
        print('|     Daftar Nilai Mahasiswa     |')
        print('==================================')


    def menu():
        system('cls')
        print('=====================================')
        print('Input Data Nilai Mahasiswa'.center(40))
        print('=====================================')
        print('|    1. Tambah Data                 |')
        print('|    2. Tampilkan Data Mahasiswa    |')
        print('|    3. Ubah Data Mahasiswa         |')
        print('|    4. Hapus Data Mahasiswa        |')
        print('|    5. Selesai                     |')
        print('=====================================')
        choose = input('Pilih Menu  : ')
        if choose == '1':
            tambah()
        elif choose == '2':
            tampilkan()
        elif choose == '3':
            ubah()
        elif choose == '4':
            hapus()
        elif choose == '5':
            selesai()
        else:
            tidak = input('Menu Tidak Ada')
            system('cls')
            menu()


    def tambah():
        system('cls')
        judul()
        print('Tambah Data'.center(40))
        print('==================================')
        nama = input('Nama     : ')
        s_nama.append(nama)
        nim = input('NIM       : ')
        s_nim.append(nim)

        system('cls')
        judul()
        print('Tambah Data'.center(40))
        print('==================================')
        tugas = float(input('Nilai Tugas    : '))
        s_tugas.append(tugas)

        uts = float(input('Nilai UTS        : '))
        s_uts.append(uts)

        uas = float(input('Nilai UAS        : '))
        s_uas.append(uas)

        total = tugas * 0.30 + uts * 0.35 + uas * 0.35
        s_akhir.append(total)
        print('Data Tersimpan'.center(40))
        kembali = input('Kembali [Enter]')
        menu()


    def tampilkan():
        system('cls')
        judul()

        for i in range(len(s_nim)):
            print('%d. Nama         : %s' % (i + 0, s_nama[i]))
            print('    NIM          : %s' % s_nim[i])
            print('    Nilai Tugas  : %.2f' % s_tugas[i])
            print('    UTS          : %.2f' % s_uts[i])
            print('    UAS          : %.2f' % s_uas[i])
            print('    Nilai Akhir  : %.2f' % s_akhir[i])
            print('-----------------------------')
        kembali = input('Kembali Tekan [Enter]')
        menu()


    def ubah():
        rubah = input('Ubah Biodata Tekan [B]   : ')
        if rubah == 'B' or rubah == 'b':
            i = int(input('Masukkan Nomor Urut  : '))
            if (i > len(s_nim[i])):
                print('Nomor Urut Salah')
            else:
                namabaru = input('Nama      : ')
                s_nama[i] = namabaru
        kembali = input('Kembali Tekan [Enter]')
        menu()


    def hapus():
        system('cls')
        judul()
        print('Hapus Data'.center(40))
        print('=================================')
        i = int(input('Masukkan Nomor Urut  : '))

        if (i > len(s_nim[i])):
            tidak = input('NIM Tidak Ada')
            hapus()

        else:
            s_nim.remove(s_nim[i])
            s_nama.remove(s_nama[i])
            s_tugas.remove(s_tugas[i])
            s_uts.remove(s_uts[i])
            s_uas.remove(s_uas[i])
            s_akhir.remove(s_akhir[i])

        print('Data Berhasil Di Hapus')
        kembali = input('Kembali Tekan [Enter]')
        menu()


    def selesai():
        system('cls')


    menu()
    
### Program :

![alt text](?raw=true)

### Hasil Run :
- Menambah data

![alt text](?raw=true)

- Menampilkan data

![alt text](?raw=true)
- Mengubah data 

![alt text](?raw=true)


- Menghapus data 

![alt text](?raw=true)
- Selesai

![alt text](?raw=true)

## Penjelasan Program :
1. Definisikan dictionary terlebih dahulu data = {}.
2. Membuat fungsi
- Fungsi tampilkan(), untuk menambahkan data def tampilkan()
- Fungsi tambah(), untuk menampilkan data def tambah()
- Fungsi hapus(nama), untuk menghapus nama pada data def hapus(nama)
- Fungsi ubah(nama), untuk mengubah nama pada data def ubah(nama)
3. Menggunakan Perulangan while True: dapat diartikan perulangan akan terus mengulang jika inputan benar dan masuk kedalam proses jika tidak maka perulangan berhenti atau lanjut ke proses selanjutnya. Gunakan statement if untuk memproses perintah yang di inginkan sesuai inputan.
4. Untuk menambahkan data pilih "[1] Tambah" gunakan fungsi if gunakan perintah "1", lalu masukan nama, nim, tugas, uts, uas, nilaiakhir, nilai akhir didapat dari = ((tugas)*30/100 + (uts)*35/100 + (uas)*35/100.
5. Lalu jika ingin memilih "[2] Lihat" gunakan fungsi 'elif' dan gunakan fungsi 'for x in data.items():' untuk melihat data pada tabel data yang kita inputkan, dengan perintah "2". Jika data tidak terdaftar maka akan tampil "TIDAK ADA DATA" atau = 0.
6. Lalu untuk menampilan pilihan "[3] Ubah" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian input nama, nim, nilai tugas, nilai uts, nilai uas untuk mengubah data nama kemudian gunakan fungsi 'else' untuk menampilkan data nama yang kita ingin ubah tidak ada.
7. Untuk menghapus data pilih "[4] Hapus" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian fungsi 'del.data[nama] jika nama yang kita hapus tidak ada dalam tabel maka gunakan fungsi 'else' untuk menampilkan "TIDAK ADA DATA".
8. Untuk keluar maka gunakan fungsi else dan exit() atau gunakan perintah [5] Keluar.
9. Selesai.

## Flowchart Praktikum 6

![Gambar WhatsApp 2022-12-06 pukul 16 17 32](https://user-images.githubusercontent.com/115867244/205897374-eb4c3775-131a-4224-a9ea-e795bac9d769.jpg)

## Sekian, Terima kasih
