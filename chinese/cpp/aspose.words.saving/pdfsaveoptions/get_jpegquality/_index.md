---
title: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality 方法"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality 方法。获取或设置决定 PDF 文档中 JPEG 图像质量的值（在 C++ 中）。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


获取或设置一个值，以确定 PDF 文档中 JPEG 图像的质量。

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## 备注


默认值为 100。

此属性与 [ImageCompression](../get_imagecompression/) 选项一起使用。

仅在文档包含 JPEG 图像时才有效。

使用此属性可在以 PDF 格式保存文档时获取或设置文档中图像的质量。该值范围为 0 到 100，其中 0 表示质量最差但压缩率最高，100 表示质量最佳但压缩率最低。如果质量为 100 且源图像为 JPEG，则表示不进行压缩——原始字节将被保存。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
