# Patch Indonesia untuk _Yuru Camp: Have a nice day!_

Ini dia yang kalian tunggu-tunggu, Patch Indonesia untuk game visual novel _Yuru Camp: Have a nice day!_.

## DISCLAIMER

> Setelah kalian memasang patch ini, kalian akan menjalankan versi **modifikasi** dari game ini.
> Pihak Nintendo dan developer tidak akan membantu, saya pun tidak akan bertanggungjawab jika terdapat crash,
> kehilangan file save, atau tiba-tiba kalian jadi ingin pergi berkemah.
>
> Ini adalah projek fanmade, yang dimana **saya tidak menjamin kualitas, kuantitas, atau fungsinya.**
> Saya terbuka dengan report bug dan memperbaiki terjemahan, silahkan buka issues dan berikan deskripsi, foto/video, serta file savedata kalian.
>
> Seluruh proses patching dapat dilakukan **sepenuhnya menggunakan data yang diperoleh secara legal**.

## DISCLAIMER (lagi)

Terjemahan ini sebagian besar menggunakan edit file manual, dan mungkin ada beberapa terjemahan yang kurang cocok karena sebagian menggunakan Google Translate.

## Baiklah, bagaimana saya membuat patchnya?

Script yang diberikan di repo ini tersedia untuk Linux/UNIX, Windows, dan Google Colab.

### Untuk Linux/UNIX
<details>
<summary>Instruksi</summary>

Bahan yang dibutuhkan :
- Python 3 dengan UnityPy terinstall (untuk `inucode.py` dan `monobehaviour_of_borg.py`)
- Wine (untuk `cpkmakec.exe`)
- [`hactool`](https://github.com/SciresM/hactool) milik SciresM untuk mengekstrak file permainan
- Original ROM, dengan format `.nsp`
- Keys dari konsol anda, berada pada direktori `$HOME/.switch`
  
Lalu jalankan perintah dibawah ini, dan file `scrpt.cpk` yang dimodifikasi akan dibuat:

```sh
./repack_scrpt.cpk.sh
```

Untuk mengekstrak file permainan dan mem-patchnya, jalankan perintah ini :

```sh
./extract_nsp.sh path/to/your/yurucamp/rom.nsp
./monobehaviour_of_borg.py
```

</details>

### Untuk Windows
<details>
<summary>Instruksi</summary>
  
Bahan yang dibutuhkan :
- Python 3 dengan UnityPy terinstall (untuk `inucode.py` dan `monobehaviour_of_borg.py`)
- .NET Framework 3.5 (untuk `cpkmakec.exe` pada Windows)
- [`hactool`](https://github.com/SciresM/hactool) milik SciresM untuk mengekstrak file permainan, simpan file exe kedalam folder `3rdparty`
- Original ROM, dengan format `.nsp`
- Keys dari konsol anda, berada pada direktori `$HOME/.switch`

Lalu jalankan perintah dibawah ini, dan file `scrpt.cpk` yang dimodifikasi akan dibuat:

```pwsh
.\repack_scrpt.cpk.ps1
```

Untuk mengekstrak file permainan dan mem-patchnya, jalankan perintah ini :

```pwsh
.\extract_nsp.ps1 path\to\your\yurucamp\rom.nsp
python3 .\monobehaviour_of_borg.py
```

</details>

### Untuk Google Colab
Klik ini untuk membaca 
      <a href="doc/Colab.md">Guide</a>

## Bagaimana saya menggunakan patch tersebut?

Setelah kalian menyelesaikan setidaknya 1 patch diatas, salin isi dari dalam folder `out`
kedalam folder `atmosphere` atau `sxos` pada SDCard Switch-mu, dan ketika kamu
menjalankan game, terjemahan seharusnya sudah terpasang.

Saya meminta maaf apabila instruksinya agak sulit dimengerti, saya mencoba untuk membuat proses patch menjadi otomatis
sebisa mungkin tanpa membagikan data hak cipta.


_(tentunya, jika kalian mencarinya, saya yakin pasti ada seseorang diluar sana yang membagikan berkas asli, tapi itu ilegal dan saya tidak bisa memaafkan itu.)_


## Terina kasih kepada

- [@Thesola10](https://github.com/Thesola10) untuk terjemahan bahasa inggris
- [@SciresM](https://github.com/SciresM) untuk `hactool`, tanpanya patch ini tidak mungkin ada
- Joseph John dan para kontributor [UnityPy](https://github.com/K0lb3/UnityPy)
- MAGES untuk gamenya
