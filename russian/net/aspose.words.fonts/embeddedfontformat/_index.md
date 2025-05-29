---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.EmbeddedFontFormat, которое определяет форматы встроенных шрифтов в объекте FontInfo для улучшенного оформления документа.
type: docs
weight: 3260
url: /ru/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Указывает формат конкретного встроенного шрифта внутри[`FontInfo`](../fontinfo/) объект.

При сохранении документа в файл записываются только встроенные шрифты соответствующего формата.

```csharp
public enum EmbeddedFontFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Определяет формат файла Embedded OpenType (EOT). |
| OpenType | `1` | Указывает шрифт, встроенный как простая копия файла шрифта OpenType (TrueType). |

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
