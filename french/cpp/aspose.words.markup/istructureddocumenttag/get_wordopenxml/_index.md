---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML méthode"
linktitle: "get_WordOpenXML"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML méthode. Obtient une chaîne qui représente le XML contenu dans le nœud au format FlatOpc en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/get_wordopenxml/
---
## IStructuredDocumentTag::get_WordOpenXML method


Obtient une chaîne qui représente le XML contenu dans le nœud au format [FlatOpc](../../../aspose.words/saveformat/).

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_WordOpenXML()=0
```


## Exemples



Montre comment obtenir le XML contenu dans le nœud au format FlatOpc.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> >()->LINQ_ToList();

ASSERT_TRUE(tags->idx_get(0)->get_WordOpenXML().Contains(u"<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"));
```

## Voir aussi

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
