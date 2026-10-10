---
title: "Aspose::Words::PlainTextDocument class"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PlainTextDocument class。允许提取文档内容的纯文本表示。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 50000
url: /zh/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


允许提取文档内容的纯文本表示。要了解更多，请访问 [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/) 文档文章。

```cpp
class PlainTextDocument : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | 获取文档的 [BuiltInDocumentProperties](./get_builtindocumentproperties/)。 |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | 获取文档的 [CustomDocumentProperties](./get_customdocumentproperties/)。 |
| [get_Text](./get_text/)() const | 获取文档的文本内容并将其连接为一个字符串。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | 从文件创建纯文本文档。自动检测文件格式。 |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 从文件创建纯文本文档。允许指定额外选项，例如加密密码。 |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | 从流创建纯文本文档。自动检测文件格式。 |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 从流创建纯文本文档。允许指定额外选项，例如加密密码。 |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
