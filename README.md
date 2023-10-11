# Patch Indonesia untuk _Yurucamp: Have a nice day!_

Ini dia yang kalian tunggu-tunggu, Patch Indonesia untuk game visual novel _Yurucamp: Have a nice day!_.

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

<summary>Windows</summary>
To build the game translation package, you will need:
- Python 3 (for `inucode.py`)
- Wine (for `cpkmakec.exe` on Linux)
- .NET Framework 3.5 (for `cpkmakec.exe` on Windows)
- Termux with proot ubuntu & box64 installed (on Android)
  
Simply run the following command, and a modified `scrpt.cpk` will be produced:

```sh
# On Linux
./repack_scrpt.cpk.sh
```
  
```pwsh
# On Windows
.\repack_scrpt.cpk.ps1
```
  
```sh
# On Android with Termux
git clone https://github.com/StevenBeach33/YC_Indonesia/
cd YC_Indonesia
bash repack_scrpt_android.cpk.sh
```
</details>

### Menus (Requires original game files)
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

## How do I install and use all that?

Once you have completed at least one of the patches above, copy the entire contents of the `out`
directory to the `atmosphere` or `sxos` directory in your Switch's SD card, and the next time you
boot up the game, the translations should apply.

I apologize if the instructions seem a bit messy, I tried automating and streamlining the patching
process as much as I could without sharing copyrighted data.


_(of course, if you were to look for it, I'm sure someone out there will end up redistributing pre-patched files, but that's illegal so I can't condone this.)_


## Special thanks

- [@Thesola10](https://github.com/Thesola10) for English translation
- [@SciresM](https://github.com/SciresM) for `hactool`, without which none of this would have been possible
- Joseph John and the [UnityPy](https://github.com/K0lb3/UnityPy) contributors
- MAGES for the game
