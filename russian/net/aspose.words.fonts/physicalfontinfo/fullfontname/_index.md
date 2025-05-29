---
title: PhysicalFontInfo.FullFontName
linktitle: FullFontName
articleTitle: FullFontName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FullFontName PhysicalFontInfo для легкого доступа к названиям шрифтов. Улучшите свою типографику с помощью точной идентификации шрифтов!
type: docs
weight: 40
url: /ru/net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

Полное название шрифта.

```csharp
public string FullFontName { get; }
```

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

* class [PhysicalFontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
