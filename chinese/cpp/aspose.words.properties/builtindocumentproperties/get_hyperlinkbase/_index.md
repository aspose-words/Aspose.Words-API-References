---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase 方法"
linktitle: "get_HyperlinkBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase 方法。指定在此文档中评估相对超链接时使用的基字符串（C++）。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


指定用于评估此文档中相对超链接的基字符串。

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## 备注


Aspose.Words 不使用此属性。

## 示例



展示如何在文档属性中存储超链接的基础部分。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入指向本地文件系统中名为 "Document.docx" 的文档的相对超链接。
// 在 Microsoft Word 中单击该链接将打开指定的文档（如果可用）。
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// 此链接是相对的。如果同一文件夹中没有 "Document.docx"
// 由于包含此链接的文档，链接将会失效。
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// 我们尝试链接的文档位于与我们计划保存文档的目录不同的目录中。
// 我们可以通过在每个链接中放置绝对文件名来修复此类链接。
// 或者，我们可以提供一个基础链接，使每个带有相对文件名的超链接
// 在点击时会在其链接前添加前缀。
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
