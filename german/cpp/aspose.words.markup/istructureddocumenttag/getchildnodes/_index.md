---
title: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes Methode"
linktitle: "GetChildNodes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes Methode. Gibt eine Live‑Sammlung von Kindknoten zurück, die den angegebenen Typen in C++ entsprechen."
type: docs
weight: 14500
url: /de/cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


Gibt eine Live‑Sammlung von Kindknoten zurück, die den angegebenen Typen entsprechen.

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
```


## Beispiele



Zeigt, wie man ein strukturiertes Dokument‑Tag entfernt, lässt jedoch den Inhalt erhalten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Diese Sammlung bietet eine einheitliche Schnittstelle zum Zugriff auf bereichsbezogene und nicht bereichsbezogene strukturierte Tags.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Hier können wir Kindknoten über die gemeinsame Schnittstelle von bereichsbezogenen und nicht bereichsbezogenen strukturierten Tags abrufen.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Siehe auch

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
