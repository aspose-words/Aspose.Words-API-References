---
title: FolderFontSource.FolderPath
second_title: Справочник по API Aspose.Words для .NET
description: FolderFontSource свойство. Путь к папке.
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Путь к папке.

```csharp
public string FolderPath { get; }
```

### Примеры

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```csharp
// Создать источник шрифта из папки, содержащей файлы шрифтов.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Смотрите также

* class [FolderFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../folderfontsource/)
* сборка [Aspose.Words](../../../)


