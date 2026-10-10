---
title: "Aspose::Words::Saving::PdfFontEmbeddingMode 枚举"
linktitle: "PdfFontEmbeddingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfFontEmbeddingMode 枚举。指定 Aspose.Words 在 C++ 中应如何嵌入字体。"
type: docs
weight: 76000
url: /zh/cpp/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enum


指定 Aspose.Words 应如何嵌入字体。

```cpp
enum class PdfFontEmbeddingMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| EmbedAll | 0 | Aspose.Words 嵌入所有字体。 |
| EmbedNonstandard | 1 | Aspose.Words 嵌入所有字体，但排除标准的 Windows 字体 Arial 和 Times New Roman。仅在此模式下影响 Arial 和 Times New Roman 字体，因为在将文档保存为 PDF 时，MS Word 并不会仅嵌入这些字体。 |
| EmbedNone | 2 | Aspose.Words 不嵌入任何字体。 |

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
