---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal méthode"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal method. Obtient une chaîne qui représente le XML contenu dans le nœud au format FlatOpc. Contrairement à la propriété WordOpenXML, cette méthode génère un document allégé qui exclut toute partie non liée au contenu en C++."
type: docs
weight: 33500
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_wordopenxmlminimal/
---
## StructuredDocumentTag::get_WordOpenXMLMinimal method


Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../../aspose.words/saveformat/). Contrairement à la propriété [WordOpenXML](../get_wordopenxml/), cette méthode génère un document allégé qui exclut toute partie non liée au contenu.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_WordOpenXMLMinimal()
```


## Exemples



Montre comment travailler avec les styles pour les éléments de contrôle de contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous deux façons d'appliquer un style du document à une balise de document structuré.
// 1 -  Appliquer un objet de style provenant de la collection de styles du document :
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Référencer un style dans le document par son nom :
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

## Voir aussi

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
