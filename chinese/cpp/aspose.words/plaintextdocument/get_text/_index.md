---
title: "Aspose::Words::PlainTextDocument::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PlainTextDocument::get_Text 方法。获取文档的文本内容，拼接为字符串，使用 C++。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


获取文档的文本内容并将其连接为一个字符串。

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## 示例



展示如何以纯文本加载 Microsoft Word 文档的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## 另见

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
