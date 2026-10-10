---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode 方法"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode 方法。指定在 C++ 中 PDF 文档的图像将如何选择颜色空间。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


指定 PDF 文档中图像的颜色空间选择方式。

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## 备注


默认值为 [Auto](../../pdfimagecolorspaceexportmode/)。

如果指定了 [SimpleCmyk](../../pdfimagecolorspaceexportmode/) 值，则会忽略 [ImageCompression](../get_imagecompression/) 选项，并对文档中的所有图像使用 Flate 压缩。

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## 另见

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
