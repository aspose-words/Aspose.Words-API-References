---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode 方法"
linktitle: "get_FontEmbeddingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode 方法。指定 C++ 中的字体嵌入模式。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


指定字体嵌入模式。

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## 备注


默认值是 [EmbedAll](../../pdffontembeddingmode/)。

此设置仅适用于 ANSI（Windows-1252）编码的文本。如果文档包含非 ANSI 文本，则无论此设置如何，都会嵌入相应的字体。

PDF/A 和 PDF/UA 合规性要求嵌入所有字体。保存为 PDF/A 和 PDF/UA 时会自动使用 [EmbedAll](../../pdffontembeddingmode/) 值。
## 另见

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
