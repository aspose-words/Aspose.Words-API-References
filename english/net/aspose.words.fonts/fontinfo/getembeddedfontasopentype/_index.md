---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words for .NET
description: Discover how the FontInfo GetEmbeddedFontAsOpenType method retrieves embedded fonts in OpenType format, enhancing your design flexibility and quality.
type: docs
weight: 100
url: /net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Gets an embedded font file in OpenType format. Fonts in Embedded OpenType format are converted to OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Parameter | Type | Description |
| --- | --- | --- |
| style | EmbeddedFontStyle | Specifies the font style to retrieve. |

### Return Value

Returns `null` if the specified font is not embedded.

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

Assert.That(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular), Is.Null);
Assert.That(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular), Is.Not.Null);

// Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### See Also

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
