---
title: Aspose::Words::Markup::MarkupLevel enum
linktitle: MarkupLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::MarkupLevel enum. Specifies the level in the document tree where a particular StructuredDocumentTag can occur in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.markup/markuplevel/
---
## MarkupLevel enum


Specifies the level in the document tree where a particular [StructuredDocumentTag](../structureddocumenttag/) can occur.

```cpp
enum class MarkupLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | 0 | Specifies the unknown or invalid value. |
| Inline | 1 | The element occurs at the inline level (e.g. among as runs of text). |
| Block | 2 | The element occurs at the block level (e.g. among tables and paragraphs). |
| Row | 3 | The element occurs among rows in a table. |
| Cell | 4 | The element occurs among cells in a row. |


## Examples



Shows how to work with styles for content control elements. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Reference a style in the document by name:
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

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
