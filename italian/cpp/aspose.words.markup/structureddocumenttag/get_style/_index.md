---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_Style"
linktitle: "get_Style"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_Style. Ottiene o imposta lo Stile del tag di documento strutturato in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_style/
---
## StructuredDocumentTag::get_Style method


Ottiene o imposta lo [Style](../../../aspose.words/style/) del tag di documento strutturato.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Markup::StructuredDocumentTag::get_Style()
```


## Esempi



Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 -  Applica un oggetto stile dalla collezione di stili del documento:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Riferisci uno stile nel documento per nome:
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

## Vedi anche

* Class [Style](../../../aspose.words/style/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
