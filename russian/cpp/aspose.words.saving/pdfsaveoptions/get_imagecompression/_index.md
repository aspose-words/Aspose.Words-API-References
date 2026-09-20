---
title: "Метод Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression"
linktitle: "get_ImageCompression"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression. Указывает тип сжатия, который будет использоваться для всех изображений в документе в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Указывает тип сжатия, используемый для всех изображений в документе.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Примечания


По умолчанию — [Auto](../../pdfimagecompression/).

Использование [Jpeg](../../pdfimagecompression/) позволяет управлять качеством изображений в результирующем документе через свойство [JpegQuality](../get_jpegquality/).

Использование [Jpeg](../../pdfimagecompression/) обеспечивает самую быструю скорость конвертации по сравнению с другими типами сжатия, однако в этом случае применяется сжатие JPEG с потерями.

Использование [Auto](../../pdfimagecompression/) позволяет контролировать качество JPEG в результирующем документе через свойство [JpegQuality](../get_jpegquality/), но для других форматов извлекаются необработанные пиксельные данные и сохраняются с сжатием Flate. Этот вариант медленнее конвертации JPEG, но без потерь.
## См. также

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
