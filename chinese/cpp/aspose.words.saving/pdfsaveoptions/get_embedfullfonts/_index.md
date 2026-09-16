---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts 方法"
linktitle: "get_EmbedFullFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts 方法。控制在 C++ 中如何将字体嵌入生成的 PDF 文档。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


控制字体如何嵌入到生成的 PDF 文档中。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## 备注


默认值为 **false**，这意味着在嵌入之前会对字体进行子集化。子集化有助于保持输出文件体积更小。如果想要更小的文件大小，子集化会移除字体中未使用的字形。

当此值设置为 **true** 时，完整的字体文件会嵌入 PDF 而不进行子集化。这会导致输出文件更大，但在需要后期编辑生成的 PDF（例如添加更多文本）时可能是有用的选项。

某些字体体积较大（数兆字节），如果不进行子集化而直接嵌入，会导致输出文档体积庞大。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
