---
title: SystemFontSource Class
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.SystemFontSource — ваш шлюз для доступа ко всем шрифтам TrueType в вашей системе для беспрепятственного создания документов.
type: docs
weight: 3480
url: /ru/net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

Представляет все шрифты TrueType, установленные в системе.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class SystemFontSource : FontSourceBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | Ctor. |
| [SystemFontSource](systemfontsource/#constructor_1)(*int*) | Ctor. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Возвращает приоритет источника шрифта. |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | Возвращает тип источника шрифта. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | Возвращает системные папки шрифтов или пустой массив, если папки недоступны. |

## Примеры

Показывает, как получить доступ к системному источнику шрифтов документа и задать замену шрифтов.

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

// Установить шрифт, который существует в каталоге шрифтов Windows, в качестве замены отсутствующему.
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
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

### Смотрите также

* class [FontSourceBase](../fontsourcebase/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
