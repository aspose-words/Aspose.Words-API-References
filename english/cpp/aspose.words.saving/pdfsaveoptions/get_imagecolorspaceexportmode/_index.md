---
title: Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method
linktitle: get_ImageColorSpaceExportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method. Specifies how the color space will be selected for the images in PDF document in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Specifies how the color space will be selected for the images in PDF document.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Remarks


The default value is [Auto](../../pdfimagecolorspaceexportmode/).

If [SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is specified, [ImageCompression](../get_imagecompression/) option is ignored and Flate compression is used for all images in the document.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## See Also

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
