---
title: Font.NameAscii
linktitle: NameAscii
second_title: Aspose.Words for .NET API Reference
description: Font NameAscii property. Returns or sets the font used for Latin text characters with character codes from 0 zero through 127 in C#.
type: docs
weight: 240
url: /net/aspose.words/font/nameascii/
---
## NameAscii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).

```csharp
public string NameAscii { get; set; }
```

## Examples

Shows how Microsoft Word can combine two different fonts in one run.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Suppose a run that we use the builder to insert while using this font configuration
// contains characters within the ASCII characters' range. In that case,
// it will display those characters using this font.
builder.Font.NameAscii = "Calibri";

// With no other font specified, the builder will also apply this font to all characters that it inserts.
Assert.AreEqual("Calibri", builder.Font.Name);

// Specify a font to use for all characters outside of the ASCII range.
// Ideally, this font should have a glyph for each required non-ASCII character code.
builder.Font.NameOther = "Courier New";

// Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
// Each character will be displayed using either of the fonts, depending on.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### See Also

* property [Name](../name/)
* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
