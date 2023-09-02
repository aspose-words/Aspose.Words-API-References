---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle enum. Specifies the style of an embedded font inside a FontInfo object in C#.
type: docs
weight: 2860
url: /net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Specifies the style of an embedded font inside a [`FontInfo`](../fontinfo/) object.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Regular | `0` | Specifies the Regular embedded font. |
| Bold | `1` | Specifies the Bold embedded font. |
| Italic | `2` | Specifies the Italic embedded font. |
| BoldItalic | `3` | Specifies the Bold-Italic embedded font. |

## Examples

Shows how to extract an embedded font from a document, and save it to the local file system.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Embedded font formats may be different in other formats such as .doc.
// We need to know the correct format before we can extract the font.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### See Also

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
