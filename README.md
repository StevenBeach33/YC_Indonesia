# Patch Indonesia untuk _Yurucamp: Have a nice day!_

Ini dia yang kalian tunggu-tunggu, Patch Indonesia untuk game visual novel _Yurucamp: Have a nice day!_.

##Patch ini belum selesai dikerjakan

## DISCLAIMER

> Setelah kalian memasang patch ini, kalian akan menjalankan versi **modifikasi** dari game ini.
> Pihak Nintendo dan developer tidak akan membantu, saya pun tidak akan bertanggungjawab jika terdapat crash,
> kehilangan file save, atau tiba-tiba kalian jadi ingin pergi berkemah.
>
> Ini adalah projek fanmade, yang dimana **saya tidak menjamin kualitas, kuantitas, atau fungsinya.**
> Saya terbuka dengan report bug dan memperbaiki terjemahan, silahkan buka issues dan berikan deskripsi, foto/video, serta savedata.
>
> Seluruh proses patching dapat dilakukan **sepenuhnya menggunakan data yang diperoleh secara legal**.

## DISCLAIMER (lagi)

Terjemahan ini sebagain besar menggunakan edit file manual, dan mungkin ada beberapa terjemahan yang kurang cocok karena sebagian menggunakan Google Translate.

## Baiklah, bagaimana saya membuat patchnya?

Script yang diberikan di repo ini tersedia untuk Linux/UNIX, Windows, dan Android w/ Termux.

### Dialog
<details>
<summary>Instruksi</summary>
Patch ini adalah untuk menerjemahkan seluruh dialog didalam game. Menu dan UI tidak akan diterjemahkan.
<details>

<details>
<summary>Linux</summary>
Bahan yang dibutuhkan :
- Python 3 (untuk `inucode.py`)
- Wine (untuk `cpkmakec.exe`)
  
Lalu jalankan perintah dibawah ini, dan file `scrpt.cpk` yang dimodifikasi akan dibuat:

```sh
./repack_scrpt.cpk.sh
```
  
<details>
<details>
<summary>Windows</summary>
Bahan yang dibutuhkan :
- Python 3 (untuk `inucode.py`)
- .NET Framework 3.5 (untuk `cpkmakec.exe` on Windows)

Lalu jalankan perintah dibawah ini, dan file `scrpt.cpk` yang dimodifikasi akan dibuat:

```pwsh
.\repack_scrpt.cpk.ps1
```
  
<details>
<details>
<summary>Android</summary>
Bahan yang dibutuhkan :
- Termux
- Koneksi internet
- Ruang tersedia ±3gb pada perangkat

Lalu jalankan perintah dibawah ini, dan file `scrpt.cpk` yang dimodifikasi akan dibuat:

```sh
????
```
</details>

### Menu dan UI (Memutuhkan file game original)
<details>
<summary>Instructions</summary>
This represents translations for the user interface components, basically everything that isn't directly
story dialogue.

To build the menu translation patch, you will need:
- Python 3 (for `monobehaviour_of_borg.py`) with `UnityPy` (run `pip install UnityPy`)
- SciresM's [`hactool`](https://github.com/SciresM/hactool) for extracting game files (on Windows, place the executable in the `3rdparty` folder)
- The original game ROM, in `.nsp` format
- Your console's cryptographic keys in the `$HOME/.switch` directory

#### Extracting game files

```sh
# On Linux
./extract_nsp.sh path/to/your/yurucamp/rom.nsp
```
  
```pwsh
# On Windows
.\extract_nsp.ps1 path\to\your\yurucamp\rom.nsp
```

```sh
# On Android w/ Termux
bash extract_nsp.sh path/to/your/yurucamp/rom.nsp
```

#### Patching game files

```sh
# On Linux
./monobehaviour_of_borg.py
```
  
```pwsh
# On Windows
python3 .\monobehaviour_of_borg.py
```

```sh
# On Android w/ Termux
python monobehaviour_of_borg.py
```

</details>

## Bagaimana saya menggunakan patch tersebut?

Setelah kalian menyelesaikan setidaknya 1 patch diatas, salin isi dari dalam folder `out`
kedalam folde `atmosphere` atau `sxos` pada SDCard Switch-mu, dan ketika kamu
menjalankan game, terjemahan seharusnya sudah terpasang.

Saya meminta maaf apabila instruksinya agak sulit dimengerti, saya mencoba untuk membuat proses patch menjadi otomatis
sebisa mungkin tanpa membagikan data copyright.


_(tentunya, jika kalian mencarinya, saya yakin pasti ada seseorang diluar sana yang membagikan berkas asli, tapi itu ilegal dan saya tidak bisa memaafkan itu.)_


## Terina kasih kepada

- [@Thesola10](https://github.com/Thesola10) untuk terjemahan bahasa inggris
- [@SciresM](https://github.com/SciresM) untuk `hactool`, tanpanya patch ini tidak mungkin ada
- Joseph John dan para kontributos [UnityPy](https://github.com/K0lb3/UnityPy)
- MAGES untuk gamenya
