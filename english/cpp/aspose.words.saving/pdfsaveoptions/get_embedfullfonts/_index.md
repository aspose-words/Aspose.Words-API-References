---
title: Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts method
linktitle: get_EmbedFullFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts method. Controls how fonts are embedded into the resulting PDF documents in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Controls how fonts are embedded into the resulting PDF documents.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Remarks


The default value is **false**, which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to **true**, a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
