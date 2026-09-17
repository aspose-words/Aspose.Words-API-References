---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal méthode"
linktitle: "get_WordOpenXMLMinimal"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal méthode. Obtient une chaîne qui représente le XML contenu dans le nœud au format FlatOpc. Contrairement à la propriété WordOpenXML, cette méthode génère un document allégé qui exclut toutes les parties non liées au contenu en C++."
type: docs
weight: 20500
url: /fr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_wordopenxmlminimal/
---
## StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal method


Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../../aspose.words/saveformat/). Contrairement à la propriété [WordOpenXML](../get_wordopenxml/), cette méthode génère un document allégé qui exclut toute partie non liée au contenu.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_WordOpenXMLMinimal()
```


## Exemples



Montre comment obtenir le XML minimal contenu dans le nœud au format FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

ASSERT_TRUE(tag->get_WordOpenXMLMinimal().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
ASSERT_FALSE(tag->get_WordOpenXMLMinimal().Contains(u"xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
```

## Voir aussi

* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
