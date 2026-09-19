---
title: "Aspose::Words::Tables::Table::EnsureMinimum metodo"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::EnsureMinimum metodo. Se la tabella non ha righe, crea e aggiunge una Row in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Se la tabella non ha righe, crea e aggiunge una [Row](../../row/).

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Esempi



Mostra come garantire che un nodo tabella contenga i nodi necessari per aggiungere contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Le tabelle contengono righe, che contengono celle, che possono contenere paragrafi
// con elementi tipici come run, forme e persino altre tabelle.
// La nostra nuova tabella non ha nessuno di questi nodi e non possiamo aggiungere contenuti finché non li ha.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Chiamare il metodo "EnsureMinimum" su una tabella garantirà che
// la tabella ha almeno una riga e una cella con un paragrafo vuoto.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
