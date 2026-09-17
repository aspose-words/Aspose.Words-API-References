---
title: "Aspose::Words::Markup::MarkupLevel énum"
linktitle: "MarkupLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::MarkupLevel enum. Spécifie le niveau dans l'arborescence du document où un StructuredDocumentTag particulier peut apparaître en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.markup/markuplevel/
---
## MarkupLevel enum


Spécifie le niveau dans l'arborescence du document où un [StructuredDocumentTag](../structureddocumenttag/) particulier peut apparaître.

```cpp
enum class MarkupLevel
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Inconnu | 0 | Spécifie la valeur inconnue ou invalide. |
| Inline | 1 | L'élément se trouve au niveau en ligne (par ex. parmi des séquences de texte). |
| Block | 2 | L'élément se trouve au niveau de bloc (par ex. parmi des tables et des paragraphes). |
| Row | 3 | L'élément se trouve parmi les lignes d'une table. |
| Cellule | 4 | L'élément se trouve parmi les cellules d'une ligne. |


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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
