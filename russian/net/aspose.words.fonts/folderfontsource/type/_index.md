---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FolderFontSource Type. Легко определяйте типы источников шрифтов, чтобы улучшить свои дизайн-проекты и оптимизировать рабочий процесс.
type: docs
weight: 40
url: /ru/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Возвращает тип источника шрифта.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
