---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Fonts.FontSourceType для эффективного управления исходным шрифтом. Оптимизируйте обработку документов с помощью гибких параметров шрифта.
type: docs
weight: 3420
url: /ru/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Указывает тип источника шрифта.

```csharp
public enum FontSourceType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| FontFile | `0` | А[`FileFontSource`](../filefontsource/) объект, представляющий один файл шрифта. |
| FontsFolder | `1` | А[`FolderFontSource`](../folderfontsource/) объект, представляющий папку с файлами шрифтов. |
| MemoryFont | `2` | А[`MemoryFontSource`](../memoryfontsource/) объект, представляющий один шрифт в памяти. |
| SystemFonts | `3` | А[`SystemFontSource`](../systemfontsource/) объект, представляющий все шрифты, установленные в системе. |
| FontStream | `4` | А[`StreamFontSource`](../streamfontsource/) объект, представляющий поток с данными шрифта. |

## Примеры

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
