---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal metod"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal metod. Hämtar en sträng som representerar XML som finns i noden i FlatOpc-formatet. Till skillnad från WordOpenXML‑egenskapen genererar den här metoden ett nedskalat dokument som utesluter alla icke‑innehållsrelaterade delar i C++."
type: docs
weight: 33500
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxmlminimal/
---
## StructuredDocumentTag::get_WordOpenXMLMinimal method


Hämtar en sträng som representerar XML som finns i noden i [FlatOpc](../../../aspose.words/saveformat/)-formatet. Till skillnad från [WordOpenXML](../get_wordopenxml/)-egenskapen genererar den här metoden ett nedskalat dokument som utesluter alla icke‑innehållsrelaterade delar.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal()
```


## Exempel



Visar hur man arbetar med stilar för innehållskontrollelement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer två sätt att applicera en stil från dokumentet på en strukturerad dokumenttagg.
// 1 -  Applicera ett stilobjekt från dokumentets stilkollektion:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Referera till en stil i dokumentet med namn:
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

## Se även

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
