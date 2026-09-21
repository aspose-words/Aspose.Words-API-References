---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode metod"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode metod. Anger hur färgrymden ska väljas för bilderna i PDF‑dokumentet i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Anger hur färgrymden kommer att väljas för bilderna i PDF-dokumentet.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Anmärkningar


Standardvärdet är [Auto](../../pdfimagecolorspaceexportmode/).

Om värdet [SimpleCmyk](../../pdfimagecolorspaceexportmode/) anges, ignoreras alternativet [ImageCompression](../get_imagecompression/) och Flate‑komprimering används för alla bilder i dokumentet.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## Se även

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
