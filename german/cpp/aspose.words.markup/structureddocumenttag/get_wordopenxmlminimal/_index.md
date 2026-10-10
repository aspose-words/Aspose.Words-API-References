---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal-Methode"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal-Methode. Gibt eine Zeichenkette zurück, die das XML darstellt, das im Knoten im FlatOpc-Format enthalten ist. Im Gegensatz zur WordOpenXML-Eigenschaft erzeugt diese Methode ein reduziertes Dokument, das alle nicht inhaltbezogenen Teile ausschließt, in C++."
type: docs
weight: 33500
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxmlminimal/
---
## StructuredDocumentTag::get_WordOpenXMLMinimal method


Gibt eine Zeichenkette zurück, die das XML darstellt, das im Knoten im [FlatOpc](../../../aspose.words/saveformat/)-Format enthalten ist. Im Gegensatz zur [WordOpenXML](../get_wordopenxml/)-Eigenschaft erzeugt diese Methode ein reduziertes Dokument, das alle nicht inhaltbezogenen Teile ausschließt.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal()
```


## Beispiele



Zeigt, wie man mit Stilen für Content-Control-Elemente arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Möglichkeiten aufgeführt, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 -  Wende ein Stilobjekt aus der Stilsammlung des Dokuments an:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Verweise im Dokument per Name auf einen Stil:
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

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
