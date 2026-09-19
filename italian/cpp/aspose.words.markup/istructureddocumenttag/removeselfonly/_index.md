---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly metodo"
linktitle: "RemoveSelfOnly"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly metodo. Rimuove solo questo nodo SDT stesso, ma mantiene il suo contenuto all'interno dell'albero del documento in C++."
type: docs
weight: 17500
url: /it/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Rimuove solo questo nodo SDT, ma mantiene il suo contenuto all'interno dell'albero del documento.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
