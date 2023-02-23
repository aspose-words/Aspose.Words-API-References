---
title: Font.NameBi
linktitle: NameBi
second_title: Aspose.Words for .NET API Reference
description: Font property. Returns or sets the name of the font in a righttoleft language document in C#.
type: docs
weight: 250
url: /net/aspose.words/font/namebi/
---
## Font.NameBi property

Returns or sets the name of the font in a right-to-left language document.

```csharp
public string NameBi { get; set; }
```

## Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Define a set of font settings for left-to-right text.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Define another set of font settings for right-to-left text.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// We can use the Bidi flag to indicate whether the text we are about to add
// with the document builder is right-to-left. When we add text with this flag set to true,
// it will be formatted using the right-to-left set of font settings.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Set the flag to false, and then add left-to-right text.
// The document builder will format these using the left-to-right set of font settings.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### See Also

* property [Name](../name/)
* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
