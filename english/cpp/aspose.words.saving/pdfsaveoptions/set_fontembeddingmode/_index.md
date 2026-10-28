---
title: Aspose::Words::Saving::PdfSaveOptions::set_FontEmbeddingMode method
linktitle: set_FontEmbeddingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_FontEmbeddingMode method. Specifies the font embedding mode in C++.'
type: docs
weight: 51000
url: /cpp/aspose.words.saving/pdfsaveoptions/set_fontembeddingmode/
---
## PdfSaveOptions::set_FontEmbeddingMode method


Specifies the font embedding mode.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_FontEmbeddingMode(Aspose::Words::Saving::PdfFontEmbeddingMode value)
```

## Remarks


The default value is [EmbedAll](../../pdffontembeddingmode/).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. [EmbedAll](../../pdffontembeddingmode/) value will be used automatically when saving to PDF/A and PDF/UA.
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
