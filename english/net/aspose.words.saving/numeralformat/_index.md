---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.NumeralFormat enum for optimal number representation in fixed page formats. Enhance your document rendering today!
type: docs
weight: 6100
url: /net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Indicates the symbol set that is used to represent numbers while rendering to fixed page formats.

```csharp
public enum NumeralFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| European | `0` | European numerals: 0123456789. |
| ArabicIndic | `1` | Numerals used in Arabic: ٠١٢٣٤٥٦٧٨٩. Unicode range U+0660 - u+0669. |
| EasternArabicIndic | `2` | Numerals used in Persian and Urdu: ۰۱۲۳۴۵۶۷۸۹. Unicode range U+06F0 - u+06F9. |
| Context | `3` | Symbol set is decided from context(locale and RTL property). |
| System | `4` | THIS OPTION IS NOT SUPPORTED. Symbol set is decided from regional settings. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
