---
title: "Aspose::Words::Tables::Cell::EnsureMinimum metodo"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Cell::EnsureMinimum metodo. Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Esempi



Mostra come garantire che un nodo cella contenga i nodi necessari per iniziare ad aggiungere contenuti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Le celle possono contenere paragrafi con elementi tipici come run, forme e persino altre tabelle.
// La nostra nuova cella non ha paragrafi, e non possiamo aggiungere contenuti come nodi run e shape finché non ne ha.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Chiamare il metodo "EnsureMinimum" su una cella garantirà che
// la cella abbia almeno un paragrafo vuoto, al quale possiamo quindi aggiungere contenuti.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Vedi anche

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
