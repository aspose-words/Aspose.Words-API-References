---
title: NumeralFormat
second_title: Aspose.Words for .NET API Reference
description: FixedPageSaveOptions property. Gets or sets NumeralFormat used for rendering of numerals. European numerals are used by default in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Gets or sets [`NumeralFormat`](../../numeralformat/) used for rendering of numerals. European numerals are used by default.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Remarks

If the value of this property is changed and page layout is already built then [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) is invoked automatically to update any changes.

## Examples

Shows how to set the numeral format used when saving to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
// use glyphs from the U+0660 to U+0669 range as numbers.
// Set the "NumeralFormat" property to "NumeralFormat.Context" to
// look up the locale to determine what number of glyphs to use.
// Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
// use glyphs from the U+06F0 to U+06F9 range as numbers.
// Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
// Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### See Also

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* assembly [Aspose.Words](../../../)
