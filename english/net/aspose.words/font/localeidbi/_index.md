---
title: Font.LocaleIdBi
linktitle: LocaleIdBi
articleTitle: LocaleIdBi
second_title: Aspose.Words for .NET
description: Discover the Font LocaleIdBi property: easily manage locale identifiers for formatted right-to-left characters, enhancing your multilingual applications.
type: docs
weight: 210
url: /net/aspose.words/font/localeidbi/
---
## Font.LocaleIdBi property

Gets or sets the locale identifier (language) of the formatted right-to-left characters.

```csharp
public int LocaleIdBi { get; set; }
```

## Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

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

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
