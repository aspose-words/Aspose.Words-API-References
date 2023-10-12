---
title: Class FontSubstitutionSettings
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.FontSubstitutionSettings сорт. Задает настройки механизма замены шрифтов.
type: docs
weight: 3010
url: /ru/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Задает настройки механизма замены шрифтов.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class FontSubstitutionSettings
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Настройки, относящиеся к правилу замены шрифтов по умолчанию. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Настройки, связанные с правилом замены конфигурации шрифта. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Настройки, связанные с правилом замены информации о шрифте. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Настройки, связанные с правилом подстановки имени шрифта. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Настройки, связанные с правилом подстановки таблиц. |

### Примечания

Процесс замены шрифта состоит из нескольких правил, которые проверяются одно за другим в определенном порядке. Если первое правило не может разрешить шрифт, проверяется второе правило и так далее.

Порядок правил следующий: 1. Правило замены имени шрифта (по умолчанию включено) 2. Правило замены конфигурации шрифта (по умолчанию отключено) 3. Правило замены таблицы (по умолчанию включено) 4. Правило замены информации о шрифте (включено по умолчанию) 5. Правило шрифта по умолчанию (включено по умолчанию)

Обратите внимание, что правило подстановки информации о шрифте всегда будет разрешать шрифт, если[`FontInfo`](../fontinfo/) isavailable и переопределит правило шрифта по умолчанию. Если вы хотите использовать правило шрифта по умолчанию, вам следует отключить правило подстановки информации о шрифте the .

Обратите внимание, что правило подстановки конфигурации шрифта в большинстве случаев разрешает шрифт и, таким образом, переопределяет все остальные правила.

### Примеры

Показывает, как получить доступ к источнику системных шрифтов документа и установить заменители шрифтов.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// По умолчанию пустой документ всегда содержит источник системного шрифта.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Установите шрифт, существующий в каталоге Windows Fonts, вместо несуществующего.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// В качестве альтернативы мы могли бы добавить папку-источник шрифта, в которой соответствующая папка содержит шрифт.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Сброс источников шрифтов по-прежнему оставляет нам системный источник шрифтов, а также наши заменители.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)


