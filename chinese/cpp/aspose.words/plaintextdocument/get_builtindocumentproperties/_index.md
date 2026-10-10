---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties 方法"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties 方法。获取文档的 BuiltInDocumentProperties（内置文档属性），使用 C++。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


获取文档的 [BuiltInDocumentProperties](./)。

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## 示例



展示如何以纯文本加载 Microsoft Word 文档的内容，然后访问原始文档的内置属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASSERT_EQ(u"John Doe", plaintext->get_BuiltInDocumentProperties()->get_Author());
```

## 另见

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
