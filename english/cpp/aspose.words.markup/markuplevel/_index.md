---
title: MarkupLevel
second_title: Aspose.Words for C++ API Reference
description: Specifies the level in the document tree where a particular StructuredDocumentTag can occur.
type: docs
weight: 209
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
SharedPtr<Style> quoteStyle = doc->get_Styles()->idx_get(StyleIdentifier::Quote);
auto sdtPlainText = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Reference a style in the document by name:
auto sdtRichText = MakeObject<StructuredDocumentTag>(doc, SdtType::RichText, MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

SharedPtr<NodeCollection> tags = doc->GetChildNodes(NodeType::StructuredDocumentTag, true);

for (const auto& node : System::IterateOver(tags))
{
    auto sdt = System::DynamicCast<StructuredDocumentTag>(node);

    ASSERT_EQ(StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words](../../)
