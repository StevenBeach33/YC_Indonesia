# Indonesia translation patch for _Yurucamp: Have a nice day!_

Here it is: the long-awaited(?) Indonesia fan-patch for the _Yurucamp: Have a nice day!_ visual novel.

## DISCLAIMER

> After applying this patch, you will be running a **modified** version of the game. Neither Nintendo nor
> the game developers will be of any help, and I will not accept responsibility for eventual crashes,
> loss of save files, or sudden urge to go camping.
>
> This is a fan-made project, provided as-is with **absolutely no guarantee of quality, fitness for a particular purpose, or even working at all.**
> Bug reports and translation fixes are welcome though.
>
> The entire patching process can be carried out **entirely using legally-obtained data**.

## DISCLAIMER (again)

The initial batch of translations was run through Google Translate. Character names have been
translated by hand wherever possible, but this is far from the best translation it could be.
If you want to take up the task of translating by hand, be my guest. The source files have been
formatted for this purpose. (You don't need to do _everything_ to file a pull request)

## Okay, how do I patch?

The scripts provided in this repository exist in both Linux/UNIX and Windows versions.

### Dialogue
<details>
<summary>Instructions</summary>
This represents translations for the actual visual novel. Menus and certain UI elements will not be translated.

To build the game translation package, you will need:
- Python 3 (for `inucode.py`)
- Wine (for `cpkmakec.exe` on Linux)
- .NET Framework 3.5 (for `cpkmakec.exe` on Windows)
  
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

#### Patching game files

```sh
# On Linux
./monobehaviour_of_borg.py
```
  
```pwsh
# On Windows
python3 .\monobehaviour_of_borg.py
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

- [@Brolijah](https://github.com/Brolijah) for YACpkTool
- [@Thesola10](https://github.com/Thesola10) for English translation
- [@SciresM](https://github.com/SciresM) for `hactool`, without which none of this would have been possible
- Joseph John and the [UnityPy](https://github.com/K0lb3/UnityPy) contributors
- MAGES for the game
