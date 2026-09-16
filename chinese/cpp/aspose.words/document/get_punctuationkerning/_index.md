---
title: "Aspose::Words::Document::get_PunctuationKerning 方法"
linktitle: "get_PunctuationKerning"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_PunctuationKerning 方法。指定在 C++ 中字距调整是否同时适用于拉丁文本和标点符号。"
type: docs
weight: 44500
url: /zh/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


指定字距调整是否同时适用于拉丁文本和标点符号。

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## 示例



展示如何处理同时适用于拉丁文本和标点符号的字距调整。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
