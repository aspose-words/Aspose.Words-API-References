---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Fonts.EmbeddedFontFormat enum. Specifies format of particular embedded font inside FontInfo object in C#.
type: docs
weight: 2720
url: /net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Specifies format of particular embedded font inside [`FontInfo`](../fontinfo/) object.

When saving a document to a file, only embedded fonts of corresponding format are written down.

```csharp
public enum EmbeddedFontFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Specifies Embedded OpenType (EOT) File Format. |
| OpenType | `1` | Specifies font, embedded as plain copy of OpenType (TrueType) font file. |

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
