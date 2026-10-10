---
title: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties 方法"
linktitle: "get_CustomDocumentProperties"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties 方法。获取文档的 CustomDocumentProperties（自定义文档属性），使用 C++。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/plaintextdocument/get_customdocumentproperties/
---
## PlainTextDocument::get_CustomDocumentProperties method


获取文档的 [CustomDocumentProperties](./)。

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::PlainTextDocument::get_CustomDocumentProperties() const
```


## 示例



展示如何以纯文本加载 Microsoft Word 文档的内容，然后访问原始文档的自定义属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_CustomDocumentProperties()->Add(u"Location of writing", System::String(u"123 Main St, London, UK"));

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASPOSE_ASSERT_EQ(u"123 Main St, London, UK", plaintext->get_CustomDocumentProperties()->idx_get(u"Location of writing")->get_Value());
```

## 另见

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
