---
title: get_StyleName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the style applied to the structured document tag.
type: docs
weight: 365
url: /cpp/aspose.words.markup/structureddocumenttag/get_stylename/
---
## StructuredDocumentTag::get_StyleName method


Gets or sets the name of the style applied to the structured document tag.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_StyleName()
```


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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
