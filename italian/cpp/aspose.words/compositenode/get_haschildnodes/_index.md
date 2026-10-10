---
title: "Metodo Aspose::Words::CompositeNode::get_HasChildNodes"
linktitle: "get_HasChildNodes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::get_HasChildNodes. Restituisce true se questo nodo ha dei nodi figlio in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode::get_HasChildNodes method


Restituisce **true** se questo nodo ha dei nodi figli.

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## Esempi



Mostra come combinare le righe di due tabelle in una sola.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 -  Dalla collezione "Tables" di un nodo Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Utilizzando il metodo "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Aggiungi tutte le righe dalla tabella corrente a quella successiva.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Rimuovi il contenitore della tabella vuota.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Vedi anche

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
