---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode метод"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode метод. Указывает, как будет выбираться цветовое пространство для изображений в PDF‑документе в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Указывает, как будет выбран цветовое пространство для изображений в PDF‑документе.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Примечания


Значение по умолчанию — [Auto](../../pdfimagecolorspaceexportmode/).

Если указано значение [SimpleCmyk](../../pdfimagecolorspaceexportmode/), параметр [ImageCompression](../get_imagecompression/) игнорируется, и для всех изображений в документе используется сжатие Flate.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## См. также

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
