# Labs6

* Berikut ini adalah flowchatnya

![gambar2](ss/ssflowchart1.png)

## Latihan 1

* Berikut adalah penjelasannya
- Dibawah ini adalah code untuk meng-import, karena kita akan gunakan system, untuk mendapatkan clear screen yang ada dalam system os, berikut code nya:

```python
from os import system
```
- Dibawah ini code untuk membuat list yang akan kita gunakan.

```python
s_nama = []
s_nim = []
s_tugas = []
s_uts = []
s_uas = []
s_akhir = []
```
- Dibawah ini code untuk membuat fungsi judul, karena didalam fungsi, kita dapat memanggil fungsi tersebut berkali-kali tanpa harus mengulang codingannya.

```python
def judul():
    print('==================================')
    print('|     Daftar Nilai Mahasiswa     |')
    print('==================================')
```
- Dibawah adalah code untuk membuat fungsi menu

```python
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
```
- berikut tampilan ketika program dijalankan

![gambar3](ss/ss3.PNG)

- code dibawah untuk membuat fungsi tambah yang ada dalam program ini

```python
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
```
- berikut tampilan ketika program dijalankan

![gambar4](ss/ss4.PNG)

- Code dibawah adalah untuk membuat fungsi tampilkan yang ada dalam program ini

```python
def tampilkan():
    system('cls')
    judul()

    for i in range(len(s_nim)):

        print('%d. Nama         : %s'%(i+0, s_nama[i]))
        print('    NIM          : %s'%s_nim[i])
        print('    Nilai Tugas  : %.2f'%s_tugas[i])
        print('    UTS          : %.2f'%s_uts[i])
        print('    UAS          : %.2f'%s_uas[i])
        print('    Nilai Akhir  : %.2f'%s_akhir[i])
        print('-----------------------------')
    kembali = input('Kembali Tekan [Enter]')
    menu()
```
- berikut tampilan ketika program dijalankan

![gambar5](ss/ss5.PNG)

- Code dibawah adalah untuk membuat fungsi merubah nama pada program ini.

```python
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
```
![gambar6](ss/ss6.PNG)    

- berikut code untuk membuat fungsi menghapus salah satu dari data dalam list.

```python
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
```
- Berikut program ketika dijalankan

![gambar7](ss/ss7.PNG)

- Dan berikut adalah program untuk fungsi mengakhiri program, dengan menekan angka 5 maka akan menyekesaikan program.

```python
def selesai():
    system('cls')
    menu()

menu()
```

### Sekian dan terima kasih

