---
title: "Metodo Aspose::Words::NodeCollection::Clear"
linktitle: "Cancella"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::NodeCollection::Clear. Rimuove tutti i nodi da questa collezione e dal documento in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Rimuove tutti i nodi da questa collezione e dal documento.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Esempi



Mostra come rimuovere tutte le sezioni da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Questo documento ha una sezione con alcuni nodi figlio che contengono e mostrano tutti i contenuti del documento.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Svuota la collezione di sezioni, il che rimuoverà tutti i figli del documento.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## Vedi anche

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
