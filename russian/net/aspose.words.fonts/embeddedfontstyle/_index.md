---
title: Enum EmbeddedFontStyle
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle перечисление. Определяет стиль встроенного шрифта внутриFontInfo объект.
type: docs
weight: 2680
url: /ru/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Определяет стиль встроенного шрифта внутри[`FontInfo`](../fontinfo/) объект.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Regular | `0` | Определяет обычный встроенный шрифт. |
| Bold | `1` | Задает полужирный встроенный шрифт. |
| Italic | `2` | Определяет встроенный курсивный шрифт. |
| BoldItalic | `3` | Определяет встроенный шрифт Bold-Italic. |

### Примеры

Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Форматы встроенных шрифтов могут отличаться в других форматах, таких как .doc.
// Нам нужно знать правильный формат, прежде чем мы сможем извлечь шрифт.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Кроме того, мы можем преобразовать встроенный формат OpenType, полученный из документов .doc, в OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)


