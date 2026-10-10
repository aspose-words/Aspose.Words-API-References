---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode method. Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Observaciones


El valor predeterminado es [Auto](../../pdfimagecolorspaceexportmode/).

Si se especifica el valor [SimpleCmyk](../../pdfimagecolorspaceexportmode/), la opción [ImageCompression](../get_imagecompression/) se ignora y se utiliza compresión Flate para todas las imágenes del documento.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## Ver también

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
