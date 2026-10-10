---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression 方法"
linktitle: "get_ImageCompression"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression 方法。指定在 C++ 中文档中所有图像使用的压缩类型。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


指定用于文档中所有图像的压缩类型。

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## 备注


默认是 [Auto](../../pdfimagecompression/)。

使用 [Jpeg](../../pdfimagecompression/) 可通过 [JpegQuality](../get_jpegquality/) 属性控制输出文档中图像的质量。

使用 [Jpeg](../../pdfimagecompression/) 与其他压缩类型相比提供最快的转换速度，但此情况下会进行有损 JPEG 压缩。

使用 [Auto](../../pdfimagecompression/) 可通过 [JpegQuality](../get_jpegquality/) 属性控制输出文档中 JPEG 的质量，但对于其他格式，会提取原始像素数据并使用 Flate 压缩保存。此方式比 JPEG 转换慢，但是无损的。
## 另见

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
