---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PhysicalFontInfo Version, легко получите доступ к строке версии шрифта для повышения согласованности дизайна и улучшения типографики.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

Строка версии шрифта.

```csharp
public string Version { get; }
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
