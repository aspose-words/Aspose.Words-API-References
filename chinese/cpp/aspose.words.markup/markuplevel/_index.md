---
title: "Aspose::Words::Markup::MarkupLevel 枚举"
linktitle: "MarkupLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::MarkupLevel 枚举。指定在 C++ 中文档树中特定 StructuredDocumentTag 可以出现的层级。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.markup/markuplevel/
---
## MarkupLevel enum


指定文档树中特定的 [StructuredDocumentTag](../structureddocumenttag/) 可以出现的层级。

```cpp
enum class MarkupLevel
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 未知 | 0 | 指定未知或无效的值。 |
| Inline | 1 | 元素出现在行内层级（例如，在文本运行之间）。 |
| 块 | 2 | 元素出现在块层级（例如，在表格和段落之间）。 |
| 行 | 3 | 元素出现在表格的行之间。 |
| 单元格 | 4 | 元素出现在行的单元格之间。 |


## 示例



展示如何使用内容控件元素的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 下面有两种方法将文档中的样式应用于结构化文档标签。
// 1 -  从文档的样式集合中应用样式对象：
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  按名称引用文档中的样式:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
