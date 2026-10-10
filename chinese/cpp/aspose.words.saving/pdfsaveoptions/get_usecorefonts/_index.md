---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts 方法"
linktitle: "get_UseCoreFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts 方法。获取或设置一个值，以确定是否在 C++ 中将 TrueType 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF Type 1 字体。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


获取或设置一个值，以确定是否用核心 PDF Type 1 字体替换 TrueType 字体 Arial、Times New Roman、Courier New 和 Symbol。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## 备注


默认值为 **false**。当此值设置为 **true** 时，PDF 文档中的 Arial、Times New Roman、Courier New 和 Symbol 字体将被相应的核心 Type 1 字体替换。

任何 PDF 查看器应用程序都需要提供核心 PDF 字体、其字体度量或合适的替代字体。

此设置仅适用于 ANSI（Windows-1252）编码的文本。非 ANSI 文本将始终使用嵌入的 TrueType 字体写入，不受此设置影响。

PDF/A 和 PDF/UA 合规性要求嵌入所有字体。保存为 PDF/A 和 PDF/UA 时将自动使用 **false** 值。

保存为 PDF 2.0 格式时不支持核心字体。保存为 PDF 2.0 时将自动使用 **false** 值。

此选项的优先级高于 [FontEmbeddingMode](../get_fontembeddingmode/) 选项。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
