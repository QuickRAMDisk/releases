# QuickRAMDisk

**[Русский](#русский) · [English](#english)**

---

## Русский

QuickRAMDisk создаёт RAM-диски в Windows 10/11 — виртуальные диски в оперативной памяти, которые работают в десятки раз быстрее SSD. Подходят для временных файлов, кэшей и сборки проектов.

В этом репозитории публикуются **готовые сборки** и принимаются **сообщения об ошибках и предложения**. Исходный код здесь не публикуется.

Сайт: [quickramdisk.pro](https://quickramdisk.pro)

### Скачать

Последняя версия — на странице [Releases](https://github.com/QuickRAMDisk/releases/releases/latest).

| Файл | Что это |
|---|---|
| `QuickRAMDisk-X.Y.Z-Setup.exe` | Установщик. Если на компьютере нет [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0), установщик скачает и поставит его сам |
| `QuickRAMDisk-X.Y.Z-Portable.exe` | Приложение без установки, .NET уже внутри |
| `QuickRAMDisk-X.Y.Z-CLI.exe` | Утилита командной строки без установки, .NET уже внутри |

**Требования:** Windows 10 (1809+) или Windows 11, x64, права администратора.

При первом запуске QuickRAMDisk устанавливает драйверы ImDisk, через которые создаются RAM-диски.

### Важно

Содержимое RAM-диска хранится только в оперативной памяти. Оно **пропадает** при выключении или перезагрузке компьютера и при удалении диска. Не храните на RAM-диске единственную копию важных данных.

### Командная строка

```powershell
# Создать RAM-диск R: размером 4 GB в NTFS
QuickRAMDisk-X.Y.Z-CLI.exe create -l R -s 4096 -f ntfs

# Список RAM-дисков
QuickRAMDisk-X.Y.Z-CLI.exe list

# Память системы и сводка по дискам
QuickRAMDisk-X.Y.Z-CLI.exe status

# Удалить диск R: без подтверждения
QuickRAMDisk-X.Y.Z-CLI.exe remove -l R --force

# Справка
QuickRAMDisk-X.Y.Z-CLI.exe --help
```

### Сообщить об ошибке или предложить улучшение

Откройте [Issue](https://github.com/QuickRAMDisk/releases/issues/new/choose) и выберите шаблон. Для ошибок приложите фрагмент лога из `%APPDATA%\QuickRAMDisk\logs` за время, когда она произошла.

### Лицензия

QuickRAMDisk — проприетарная программа. Условия использования — в [лицензионном соглашении](EULA.md) (также на [сайте](https://quickramdisk.pro/eula.html?lang=ru)). Бесплатная версия Free — для личного некоммерческого использования.

Сторонние компоненты: [ImDisk Toolkit](https://ltr-data.se/opencode.html/) (MIT License, © Olof Lagerkvist).

© 2026 QuickRAMDisk Team · [dev@quickramdisk.pro](mailto:dev@quickramdisk.pro)

---

## English

QuickRAMDisk creates RAM disks on Windows 10/11 — virtual disks in memory that are dozens of times faster than an SSD. Useful for temporary files, caches and builds.

This repository hosts **ready-to-use builds** and accepts **bug reports and feature requests**. The source code is not published here.

Website: [quickramdisk.pro](https://quickramdisk.pro/en/)

### Download

Get the latest version on the [Releases](https://github.com/QuickRAMDisk/releases/releases/latest) page.

| File | What it is |
|---|---|
| `QuickRAMDisk-X.Y.Z-Setup.exe` | Installer. If the [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/8.0) is missing, the installer downloads and installs it for you |
| `QuickRAMDisk-X.Y.Z-Portable.exe` | Application without installation, .NET included |
| `QuickRAMDisk-X.Y.Z-CLI.exe` | Command-line tool without installation, .NET included |

**Requirements:** Windows 10 (1809+) or Windows 11, x64, administrator rights.

On first run QuickRAMDisk installs the ImDisk drivers it uses to create RAM disks.

### Important

A RAM disk lives only in memory. Its contents are **lost** when the computer is shut down or restarted and when the disk is removed. Do not keep the only copy of important data on a RAM disk.

### Command line

```powershell
# Create a 4 GB NTFS RAM disk R:
QuickRAMDisk-X.Y.Z-CLI.exe create -l R -s 4096 -f ntfs

# List RAM disks
QuickRAMDisk-X.Y.Z-CLI.exe list

# System memory and disk summary
QuickRAMDisk-X.Y.Z-CLI.exe status

# Remove disk R: without confirmation
QuickRAMDisk-X.Y.Z-CLI.exe remove -l R --force

# Help
QuickRAMDisk-X.Y.Z-CLI.exe --help
```

### Report a bug or suggest an improvement

Open an [issue](https://github.com/QuickRAMDisk/releases/issues/new/choose) and choose a template. For bugs, attach the relevant part of the log from `%APPDATA%\QuickRAMDisk\logs`.

### License

QuickRAMDisk is proprietary software. See the [License Agreement](EULA.md) (also on the [website](https://quickramdisk.pro/eula.html?lang=en)). The free edition is for personal non-commercial use.

Third-party components: [ImDisk Toolkit](https://ltr-data.se/opencode.html/) (MIT License, © Olof Lagerkvist).

© 2026 QuickRAMDisk Team · [dev@quickramdisk.pro](mailto:dev@quickramdisk.pro)
