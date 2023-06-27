# Guide-XUnity.AutoTranslator-and-BepInEx-for-il2cpp-games
Guide how to run XUnity.AutoTranslator with BepInEx for il2cpp games.

1. Download [archive](https://mega.nz/file/0ZM3CIjA#KyAW9VeEHwAotszTqglDSHuAFeNogaUIGwDnEdK3FCw) with all-in-package.
2. Unzip it in the game's root directory (with \*Game name\*_Data folder and \*Game name\*.exe file).
3. Go to the \BepInEx\config folder and modify AutoTranslatorConfig.ini how you see it fit. (You can check detailed explanation for each option [here](https://github.com/bbepis/XUnity.AutoTranslator#configuration))
4. Run *Game name\*.exe and wait for initial BepInEx hooks and settings to apply.
5. Enjoy!

## How to use Sugoi Translator offline with CUDA

You can follow guide [here](https://github.com/Vin-meido/XUnity-AutoTranslator-SugoiOfflineTranslatorEndpoint) if you just need standard Sugoi Transaltor (no CUDA).
Or you can follow my instruction for step by step guide for **Sugoi-Toolkit-V6.0** (different version will most likely need another instruction). 

1. Download Sugoi-Toolkit-V6.0 from [Google Drive](https://drive.google.com/file/d/1VHNkRLrIXUbZBaD1ETHDqowfzk3GZ21b/view?usp=sharing) or [mirror server](https://sugoi-file.sfo3.cdn.digitaloceanspaces.com/Sugoi-Translator-Toolkit-V6.0-Anniversary.rar). If links are outdated check out author's [patreon](https://www.patreon.com/mingshiba/about).
2. Unzip it to a folder with a prefferably short name (i.e. C:/Games/SugoiV6.0/).
3. Download [CUDA 11.8](https://developer.nvidia.com/cuda-11-8-0-download-archive) and [cuDNN 8.8.0](https://developer.download.nvidia.com/compute/redist/cudnn/v8.8.0/local_installers/11.8/) for that version then install both.
4. Download [archive](https://cdn.discordapp.com/attachments/795551389211164703/1122512373719236658/CudaInstallForToolKit6.zip) with script which will install all Python CUDA libs for Sugoi Translator.
5. Unzip it to a folder where you extracted Sugoi Translator before (i.e. C:/Games/SugoiV6.0/CudaInstall)
6. Run C:/Games/SugoiV6.0/CudaInstall/install-cuda.ps1 from PowerShell and pick "2: Install Cuda". In popup window pick SugoiV6.0 folder (i.e. C:/Games/SugoiV6.0/). It will take some time to download all libs and install them.
7. Run that script again and pick "11: Install: Cuda Script". In popup window pick SugoiV6.0 folder (i.e. C:/Games/SugoiV6.0/). Now we will install Ctranslate2 for even better performance.
8. Run that script again and pick "5: Install Ctranslate2". In popup window pick SugoiV6.0 folder (i.e. C:/Games/SugoiV6.0/). It will take some time to download all libs and install them.
9. Finally, run Sugoi-Translator-Offline-CT2 (click here).bat in C:/Games/SugoiV6.0/, pick "20. Change to cuda" and pick "1.Sugoi Translator Offline CTranslate2" to launch offline server translator.
10. For XUnity.AutoTranslator to use Sugoi Translator change Endpoint in \BepInEx\config\AutoTranslatorConfig.ini from GoogleTranslate to SugoiOfflineTranslator (i.e. Endpoint=SugoiOfflineTranslator).
11. Run game and enjoy!
