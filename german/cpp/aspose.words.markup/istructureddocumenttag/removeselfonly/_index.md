---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly Methode"
linktitle: "RemoveSelfOnly"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly Methode. Entfernt nur diesen SDT‑Knoten selbst, lässt jedoch dessen Inhalt im Dokumentbaum in C++ erhalten."
type: docs
weight: 17500
url: /de/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Entfernt nur diesen SDT‑Knoten selbst, lässt jedoch den Inhalt im Dokumentbaum erhalten.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
