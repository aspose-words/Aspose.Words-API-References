---
title: "Aspose::Words::Markup::MarkupLevel enum"
linktitle: "MarkupLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::MarkupLevel enum. Anger nivån i dokumentträdet där en viss StructuredDocumentTag kan förekomma i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.markup/markuplevel/
---
## MarkupLevel enum


Anger nivån i dokumentträdet där en viss [StructuredDocumentTag](../structureddocumenttag/) kan förekomma.

```cpp
enum class MarkupLevel
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Okänd | 0 | Anger det okända eller ogiltiga värdet. |
| Inbäddad | 1 | Elementet förekommer på inline-nivå (t.ex. bland textsekvenser). |
| Block | 2 | Elementet förekommer på blocknivå (t.ex. bland tabeller och stycken). |
| Row | 3 | Elementet förekommer bland rader i en tabell. |
| Cell | 4 | Elementet förekommer bland celler i en rad. |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
