---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FolderFontSource ScanSubfolders, чтобы легко управлять организацией шрифтов, выбирая сканирование подпапок для повышения эффективности.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Определяет, следует ли сканировать подпапки.

```csharp
public bool ScanSubfolders { get; }
```

## Примеры

Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.

```csharp
// Создаем источник шрифтов из папки, содержащей файлы шрифтов.
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
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
