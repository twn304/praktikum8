## Praktikum 8

## Input 
1. Pertama buat deklarai class

```py

class Mahasiswa:
    nama = ""
    nim =""
    uts =""
    uas =""
    tugas = ""
    akhir = ""

```
2. Membuat list kosong data mahasiswa

```py
DataMahasiswa = []
```
3. Membuat fungsi tambah data
```py
def add():
    system("cls")
    Mhs = Mahasiswa()
    print("TAMBAH DATA")

    Mhs.nama = input("Nama        : ")
    Mhs.nim  = input("NIM         : ")
    Mhs.tugas = int(input("Nilai Tugas : "))
    Mhs.uts = int(input("Nilai UTS   : "))
    Mhs.uas = int(input("Nilai UAS   : "))
    Mhs.akhir = (Mhs.tugas * 30/100) + (Mhs.uts * 35/100) + (Mhs.uas * 35/100)

    DataMhs.append(Mhs)
```
4. Membuat fungsi tampilkan data sesudah di input
```py
def show():
    system("cls")
    print("      DAFTAR NILAI MAHASISWA")
    if len(DataMhs) <= 0:
        print("=================================")
        print("         TIDAK ADA DATA")
        print("\n")
        print("=================================")
    else:
        for Mhs in DataMhs:
            print("=================================")
            print("Nama        : {} ".format(Mhs.nama))
            print("NIM         : {} ".format(Mhs.nim))
            print("Nilai Tugas : {} ".format(Mhs.tugas))
            print("Nilai UTS   : {} ".format(Mhs.uts))
            print("Nilai UAS   : {} ".format(Mhs.uas))
            print("Nilai Akhir : {:.1f} ".format(Mhs.akhir))
            print("=================================")
```
5. Membuat fungsi untuk menghapus data
```py
def delete():
    system("cls")
    print("HAPUS DATA")
    nama = Mahasiswa()
    nama = input("Nama : ")
    for data in DataMhs:
        if nama == data.nama:
            DataMhs.remove(data)

            print("Berhasil Dihapus")
    
        else:
            print("DATA TIDAK DITEMUKAN")
```
6. Membuat fungsi untuk mengubah data
```py
def update():
    system("cls")
    print("UBAH DATA")
    nama = Mahasiswa()
    nama = input("Nama : ")
    print("\n")

    for data in DataMhs:
        if nama == data.nama:
            data.tugas = int(input("Nilai Tugas : "))
            data.uts = int(input("Nilai UTS   : "))
            data.uas = int(input("Nilai UAS   : "))
            data.akhir = (data.tugas * 30/100) + (data.uts * 35/100) + (data.uas * 35/100)

            print("DATA BERHASIL DIUBAH")

        else:
            print("DATA TIDAK DITEMUKAN")
```
7.Program looping (Perulangan) menggunakan while
```py
while True:
    print("\n")
    print("==========================")
    print("    Program Input Nilai   ")
    print("==========================")

    print("[1] LIHAT DATA")
    print("[2] TAMBAH DATA")
    print("[3] UBAH DATA ")
    print("[4] HAPUS DATA")
    print("[5] KELUAR ")

    ask = input("PILIH MENU >")

    if ask == '1':
        show()

    elif ask == '2':
        add()
    
    elif ask == '3':
        update()
    
    elif ask == '4':
        delete()
    
    elif ask == '5':
        print("\n")
        print("selesai")

        exit()

    else:
```
