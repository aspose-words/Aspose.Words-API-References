---
title: "Método Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality"
linktitle: "get_JpegQuality"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality. Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Observaciones


El valor predeterminado es 100.

Esta propiedad se usa junto con la opción [ImageCompression](../get_imagecompression/).

Tiene efecto solo cuando un documento contiene imágenes JPEG.

Utilice esta propiedad para obtener o establecer la calidad de las imágenes dentro de un documento al guardarlo en formato PDF. El valor puede variar de 0 a 100, donde 0 significa la peor calidad pero máxima compresión y 100 significa la mejor calidad pero mínima compresión. Si la calidad es 100 y la imagen de origen es JPEG, significa que no hay compresión; se guardarán los bytes originales.
## Ver también

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
