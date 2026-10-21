# 🇷🇺 Pixel UI Russian Localization by GoldenFrog

Исходники русификации интерфейса Google Pixel и Pixel-подобных прошивок: переведённые строки и манифесты 19 RRO-оверлеев из Magisk-модуля **Pixel UI Russian Localization**.

Модуль исправляет пропущенные, частично переведённые и неточные строки в системных компонентах. Это настройки, системный интерфейс, лаунчер, Android System Intelligence и сервисы Pixel.

**Текущая версия модуля:** 1.7_05.10.26 (versionCode 37).

Проверено на реальном устройстве:

* **Google Pixel 8 Pro** (husky, Tensor G3), Android 17, Magisk

## ⚠️ Важно

* Не рекомендуется использовать одновременно с другими модулями локализации или overlay-пакетами, затрагивающими те же компоненты.
* Оверлей привязан к **имени пакета** (`com.android.settings`, `com.android.systemui` и т. д.), а не к конкретному APK. Поэтому на AOSP-прошивках он тоже применится. Заменятся только те строки, которые в этой прошивке есть. Строки, специфичные для Google или переименованные между версиями Android, просто не переведутся. Ничего при этом не ломается.
* Сборка оверлеев — под Android 17 (префикс `a17` в именах APK модуля). На более старых версиях часть строк может не совпасть по именам.

## 🎯 Совместимость

* Android 13 и выше (`minSdk 33`)
* В приоритете: устройства Google Pixel и «чистые» прошивки, близкие к стоковому Pixel (в духе Pixel Experience Plus)
* Остальные устройства: там, где оверлеи могут «натянуться» на системные компоненты
* Тип установки: Magisk-модуль (статические RRO-оверлеи в `/system/product/overlay`)
* Не предназначено для MIUI / HyperOS, One UI и других сильно изменённых оболочек

## 🌟 Ключевые особенности

* **19 оверлеев**: от `framework-res` и `SettingsGoogle` до сервисов Pixel.
* **Около 22 900 строк**, массивов и plurals; больше всего — в настройках (18 069) и системном интерфейсе (3 618).
* **Чистая установка**: метод RRO не трогает раздел `/system` напрямую, работая через Magisk.
* **Открытые исходники**: каждую строку можно посмотреть, сравнить между версиями и предложить исправление.

## 📦 Список локализованных компонентов

<details>
<summary>Нажмите, чтобы развернуть список (19 оверлеев)</summary>

| Оверлей | Целевой пакет | Строк |
|---|---|---|
| `framework-res` | `android` | 69 |
| `SettingsGoogle` | `com.android.settings` | 18 069 |
| `SettingsIntelligenceGooglePrebuilt` | `com.google.android.settings.intelligence` | 4 |
| `SystemUIGoogle` | `com.android.systemui` | 3 618 |
| `NexusLauncherRelease` | `com.google.android.apps.nexuslauncher` | 522 |
| `DevicePersonalizationPrebuiltPixel` | `com.google.android.as` | 484 |
| `DownloadProvider` | `com.android.providers.downloads` | 44 |
| `NowPlayingPrebuilt` | `com.google.android.apps.pixel.nowplaying` | 28 |
| `PixelSupportPrebuilt` | `com.google.android.apps.pixel.support` | 24 |
| `EasterEgg` | `com.android.egg` | 20 |
| `WallpaperPickerGoogleRelease` | `com.google.android.apps.wallpaper` | 16 |
| `SoundPickerPrebuilt` | `com.google.android.soundpicker` | 7 |
| `GoogleCamera` | `com.google.android.GoogleCamera` | 5 |
| `RelationshipsPrebuilt` | `com.google.android.apps.pixel.relationships` | 5 |
| `AiIconsPrebuilt` | `com.google.android.apps.ai.icons` | 2 |
| `ANGLE` | `com.android.angle` | 1 |
| `DeviceConnectivityServicePrebuilt` | `com.google.android.apps.pixel.dcservice` | 1 |
| `RepairMode` | `com.google.android.repairmode` | 1 |
| `WallpaperEmojiPrebuilt` | `com.google.android.apps.emojiwallpaper` | 1 |

</details>

## 📁 Структура репозитория

```
overlays/
  <Оверлей>/
    AndroidManifest.xml          # целевой пакет, приоритет 1000, isStatic
    res/values-ru/strings.xml    # + arrays.xml, plurals.xml, где есть
module/
  module.prop                    # id, версия, описание модуля
  META-INF/com/google/android/   # установщик Magisk
```

В репозитории только исходники: переведённые строки и манифесты. Собранные APK и готовый ZIP модуля сюда не входят.

## 🛠 Установка

1. Прошейте модуль через **Magisk**.
2. Перезагрузите устройство.

## 🧹 Удаление

1. Отключите или удалите модуль в **Magisk**.
2. Перезагрузите устройство.

---

## 📄 Лицензия

Проект распространяется по лицензии MIT: переводы можно свободно использовать, изменять и распространять, в том числе в коммерческих целях, при сохранении уведомления об авторских правах. Переводы предоставляются «как есть», без каких-либо гарантий.

Названия Google, Pixel, Android и связанные с ними товарные знаки принадлежат их правообладателям.
