---
title: PhysicalFontInfo.FullFontName
second_title: Справочник по API Aspose.Words для .NET
description: PhysicalFontInfo свойство. Полное название шрифта.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

Полное название шрифта.

```csharp
public string FullFontName { get; }
```

### Примеры

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
* пространство имен [Aspose.Words.Fonts](../../physicalfontinfo/)
* сборка [Aspose.Words](../../../)


