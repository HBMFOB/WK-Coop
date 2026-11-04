# Third-party components

[Русский](#сторонние-компоненты) | **English**

`WKCoop-Setup-*.exe` contains the official BepInEx 5.4.23.6 archive for Windows x64, unmodified. The installer unpacks it into the game folder. The installer contains no game files.

| Component | Files | License | License text | Source code |
|---|---|---|---|---|
| BepInEx 5.4.23.6 | `BepInEx.*.dll` | LGPL-2.1 | [text](licenses/BepInEx-LICENSE.txt) | https://github.com/BepInEx/BepInEx |
| UnityDoorstop 4.6.0 | `winhttp.dll` | LGPL-2.1 | [text](licenses/UnityDoorstop-LICENSE.txt) | https://github.com/NeighTools/UnityDoorstop |
| HarmonyX | `0Harmony*.dll`, `HarmonyXInterop.dll` | MIT | [text](licenses/HarmonyX-LICENSE.txt) | https://github.com/BepInEx/HarmonyX |
| MonoMod | `MonoMod.*.dll` | MIT | [text](licenses/MonoMod-LICENSE.txt) | https://github.com/MonoMod/MonoMod |
| Mono.Cecil | `Mono.Cecil*.dll` | MIT | [text](licenses/Mono.Cecil-LICENSE.txt) | https://github.com/jbevain/cecil |

The mod is installed into the game folder as a separate file and does not modify these libraries, so they can be replaced with your own build of the same version.

## Player models

`WKCoop.dll` contains four player models converted for the mod (meshes and textures). They are fan works by their authors; no license was supplied with them, and all rights stay with the authors and the character owners.

| Model | Author / source |
|---|---|
| Miku (`miku`) | "Hatsune Miku (Half Life) (Playermodel/Ragdoll)" for Garry's Mod by xinus22. Hatsune Miku is a character of Crypton Future Media |
| Teto (`teto`) | "Kasane Teto (Playermodel/Ragdoll) (Half Life)" for Garry's Mod by xinus22. Kasane Teto is a character of TWINDRILL |
| Carrot (`luuvan`) | "Luuvan" carrot character (Maya scene), author not stated in the files |
| Harpy (`harpy`) | "Harpy" (FBX), author not stated in the files |

If you are an author and do not want your model in the mod, open an issue and it will be removed.

# Сторонние компоненты

`WKCoop-Setup-*.exe` содержит официальный архив BepInEx 5.4.23.6 для Windows x64 без изменений. Установщик распаковывает его в папку игры. Файлов игры в установщике нет.

| Компонент | Файлы | Лицензия | Текст лицензии | Исходный код |
|---|---|---|---|---|
| BepInEx 5.4.23.6 | `BepInEx.*.dll` | LGPL-2.1 | [текст](licenses/BepInEx-LICENSE.txt) | https://github.com/BepInEx/BepInEx |
| UnityDoorstop 4.6.0 | `winhttp.dll` | LGPL-2.1 | [текст](licenses/UnityDoorstop-LICENSE.txt) | https://github.com/NeighTools/UnityDoorstop |
| HarmonyX | `0Harmony*.dll`, `HarmonyXInterop.dll` | MIT | [текст](licenses/HarmonyX-LICENSE.txt) | https://github.com/BepInEx/HarmonyX |
| MonoMod | `MonoMod.*.dll` | MIT | [текст](licenses/MonoMod-LICENSE.txt) | https://github.com/MonoMod/MonoMod |
| Mono.Cecil | `Mono.Cecil*.dll` | MIT | [текст](licenses/Mono.Cecil-LICENSE.txt) | https://github.com/jbevain/cecil |

Мод ставится в папку игры отдельным файлом и не изменяет эти библиотеки, поэтому их можно заменить своей сборкой той же версии.

## Модели игроков

В `WKCoop.dll` вшиты четыре модели игроков, переделанные для мода (сетки и текстуры). Это фанатские работы их авторов; лицензии к ним не прилагалось, все права остаются за авторами и правообладателями персонажей.

| Модель | Автор / источник |
|---|---|
| Мику (`miku`) | «Hatsune Miku (Half Life) (Playermodel/Ragdoll)» для Garry's Mod, автор xinus22. Хацунэ Мику — персонаж Crypton Future Media |
| Тето (`teto`) | «Kasane Teto (Playermodel/Ragdoll) (Half Life)» для Garry's Mod, автор xinus22. Касанэ Тето — персонаж TWINDRILL |
| Морковка (`luuvan`) | персонаж-морковка «Luuvan» (сцена Maya), автор в файлах не указан |
| Гарпия (`harpy`) | «Harpy» (FBX), автор в файлах не указан |

Если вы автор и не хотите, чтобы ваша модель была в моде, напишите в issues — её уберут.
