---
title: Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression method
linktitle: get_ImageCompression
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression method. Specifies compression type to be used for all images in the document in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


Specifies compression type to be used for all images in the document.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## Remarks


Default is [Auto](../../pdfimagecompression/).

Using [Jpeg](../../pdfimagecompression/) lets you control the quality of images in the output document through the [JpegQuality](../get_jpegquality/) property.

Using [Jpeg](../../pdfimagecompression/) provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using [Auto](../../pdfimagecompression/) lets to control the quality of Jpeg in the output document through the [JpegQuality](../get_jpegquality/) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless. 
## See Also

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
