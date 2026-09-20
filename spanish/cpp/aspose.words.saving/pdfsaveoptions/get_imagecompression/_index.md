---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression"
linktitle: "get_ImageCompression"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression. Especifica el tipo de compresión que se utilizará para todas las imágenes del documento en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Especifica el tipo de compresión que se usará para todas las imágenes del documento.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Observaciones


El valor predeterminado es [Auto](../../pdfimagecompression/).

Usar [Jpeg](../../pdfimagecompression/) le permite controlar la calidad de las imágenes en el documento de salida mediante la propiedad [JpegQuality](../get_jpegquality/).

Usar [Jpeg](../../pdfimagecompression/) proporciona la velocidad de conversión más rápida en comparación con el rendimiento de otros tipos de compresión, pero en este caso hay compresión JPEG con pérdida.

Usar [Auto](../../pdfimagecompression/) permite controlar la calidad del Jpeg en el documento de salida mediante la propiedad [JpegQuality](../get_jpegquality/), pero para otros formatos, los datos de píxeles sin procesar se extraen y se guardan con compresión Flate. Este caso es más lento que la conversión Jpeg pero sin pérdida.
## Ver también

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
