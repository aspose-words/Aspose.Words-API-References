---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words для .NET
description: Aspose.Words.Fonts.PhysicalFontInfo сорт. Указывает информацию о физическом шрифте доступном для механизма шрифтов Aspose.Words на С#.
type: docs
weight: 3030
url: /ru/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Указывает информацию о физическом шрифте, доступном для механизма шрифтов Aspose.Words.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class PhysicalFontInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Путь к файлу шрифта, если есть. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Фамилия шрифта. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Полное название шрифта. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Строка версии шрифта. |

## Примеры

Показывает, как составить список доступных шрифтов.

```csharp
// Настройте Aspose.Words для получения шрифтов из пользовательской папки, а затем распечатайте каждый доступный шрифт.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
