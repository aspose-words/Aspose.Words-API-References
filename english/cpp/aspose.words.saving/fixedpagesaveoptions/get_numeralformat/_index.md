---
title: get_NumeralFormat
second_title: Aspose.Words for C++ API Reference
description: Gets or sets NumeralFormat used for rendering of numerals. European numerals are used by default.
type: docs
weight: 66
url: /cpp/aspose.words.saving/fixedpagesaveoptions/get_numeralformat/
---
## FixedPageSaveOptions::get_NumeralFormat method


Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals. European numerals are used by default.

```cpp
Aspose::Words::Saving::NumeralFormat Aspose::Words::Saving::FixedPageSaveOptions::get_NumeralFormat() const
```


## Examples



Shows how to set the numeral format used when saving to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_LocaleId(MakeObject<System::Globalization::CultureInfo>(u"ar-AR")->get_LCID());
builder->Writeln(u"1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
// use glyphs from the U+0660 to U+0669 range as numbers.
// Set the "NumeralFormat" property to "NumeralFormat.Context" to
// look up the locale to determine what number of glyphs to use.
// Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
// use glyphs from the U+06F0 to U+06F9 range as numbers.
// Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
// Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
options->set_NumeralFormat(numeralFormat);

doc->Save(ArtifactsDir + u"PdfSaveOptions.SetNumeralFormat.pdf", options);
```

## See Also

* Enum [NumeralFormat](../../numeralformat/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
