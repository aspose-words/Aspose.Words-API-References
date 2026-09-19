---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal method"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal method. Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato FlatOpc. A differenza della proprietà WordOpenXML, questo metodo genera un documento semplificato che esclude tutte le parti non relative al contenuto in C++."
type: docs
weight: 33500
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxmlminimal/
---
## StructuredDocumentTag::get_WordOpenXMLMinimal method


Restituisce una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../../aspose.words/saveformat/). A differenza della proprietà [WordOpenXML](../get_wordopenxml/), questo metodo genera un documento semplificato che esclude tutte le parti non relative al contenuto.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal()
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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
