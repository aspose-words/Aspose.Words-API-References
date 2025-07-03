---
title: Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality method
linktitle: get_JpegQuality
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality method. Gets or sets a value determining the quality of the JPEG images inside PDF document in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Gets or sets a value determining the quality of the JPEG images inside PDF document.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Remarks


The default value is 100.

This property is used in conjunction with the [ImageCompression](../get_imagecompression/) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression. If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
