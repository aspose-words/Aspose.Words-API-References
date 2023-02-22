---
title: FontSourceBase.GetAvailableFonts
second_title: Справочник по API Aspose.Words для .NET
description: FontSourceBase метод. Возвращает список шрифтов доступных через этот источник.
type: docs
weight: 40
url: /ru/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Возвращает список шрифтов, доступных через этот источник.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* пространство имен [Aspose.Words.Fonts](../../fontsourcebase/)
* сборка [Aspose.Words](../../../)


