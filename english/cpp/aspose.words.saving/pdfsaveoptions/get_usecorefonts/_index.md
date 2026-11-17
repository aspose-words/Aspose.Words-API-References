---
title: Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts method
linktitle: get_UseCoreFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts method. Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts in C++.'
type: docs
weight: 32000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Remarks


The default value is **false**. When this value is set to **true** Arial, Times New Roman, Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. **false** value will be used automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format. **false** value will be used automatically when saving to PDF 2.0.

This option has a higher priority then [FontEmbeddingMode](../get_fontembeddingmode/) option. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
