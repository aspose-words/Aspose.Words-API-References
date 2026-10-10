---
title: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method"
linktitle: "GetChildNodes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes method. Restituisce una collezione live di nodi figlio che corrispondono ai tipi specificati in C++."
type: docs
weight: 14500
url: /it/cpp/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag::GetChildNodes method


Restituisce una collezione live di nodi figlio che corrispondono ai tipi specificati.

```cpp
virtual System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::IStructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)=0
```


## Esempi



Mostra come rimuovere il tag di documento strutturato, ma mantiene il contenuto interno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Questa collezione fornisce un'interfaccia unificata per accedere ai tag strutturati con intervallo e senza intervallo.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Qui possiamo ottenere i nodi figlio dall'interfaccia comune dei tag strutturati con intervallo e senza intervallo.
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

## Vedi anche

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
