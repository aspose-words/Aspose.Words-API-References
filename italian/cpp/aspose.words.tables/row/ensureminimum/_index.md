---
title: "Metodo Aspose::Words::Tables::Row::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Row::EnsureMinimum. Se la Row non ha celle, crea e aggiunge una Cell in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Se la [Row](../) non ha celle, crea e aggiunge una [Cell](../../cell/).

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Esempi



Mostra come garantire che un nodo row contenga i nodi di cui abbiamo bisogno per iniziare ad aggiungere contenuti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Le Rows contengono celle, contenenti paragrafi con elementi tipici come run, shapes e persino altre tabelle.
// La nostra nuova row non ha nessuno di questi nodi, e non possiamo aggiungere contenuti finché non li ha.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Chiamare il metodo "EnsureMinimum" su una tabella garantirà che
// la tabella ha almeno una cell con un paragrafo vuoto.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Vedi anche

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
