---
title: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat method"
linktitle: "get_DefaultParagraphFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat method. 在 C++ 中获取文档的默认段落格式。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/stylecollection/get_defaultparagraphformat/
---
## StyleCollection::get_DefaultParagraphFormat method


获取文档默认的段落格式。

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::StyleCollection::get_DefaultParagraphFormat()
```

## 备注


请注意，文档范围的默认设置是在 Microsoft Word 2007 中引入的，仅在 OOXML 格式（[Docx](../../loadformat/)）中得到完整支持。早期的文档格式不支持文档默认段落格式。

## 示例



展示如何向文档的样式集合添加一个 [Style](../../style/)。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// 为我们以后可能添加到此集合的新样式设置默认参数。
styles->get_DefaultFont()->set_Name(u"Courier New");
// 如果我们添加一个 \"StyleType.Paragraph\" 类型的样式，集合将应用这些值。
// 其 \"DefaultParagraphFormat\" 属性到样式的 \"ParagraphFormat\" 属性。
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// 添加一个样式，然后验证它具有默认设置。
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## 另见

* Class [ParagraphFormat](../../paragraphformat/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
