---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words EmbeddedFontStyle, которое позволяет легко управлять встроенными стилями шрифтов в объектах FontInfo, расширяя возможности форматирования документов.
type: docs
weight: 3270
url: /ru/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Задает стиль встроенного шрифта внутри[`FontInfo`](../fontinfo/) объект.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Regular | `0` | Указывает обычный встроенный шрифт. |
| Bold | `1` | Указывает жирный встроенный шрифт. |
| Italic | `2` | Указывает курсивный встроенный шрифт. |
| BoldItalic | `3` | Задает полужирный курсивный встроенный шрифт. |

## Примеры

Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Форматы встроенных шрифтов могут отличаться в других форматах, таких как .doc.
// Прежде чем извлечь шрифт, нам нужно знать правильный формат.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Кроме того, мы можем преобразовать встроенный формат OpenType, который получен из документов .doc, в OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
