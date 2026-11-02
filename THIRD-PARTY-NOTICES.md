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
