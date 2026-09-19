---
title: "Aspose::Words::Tables::Table::Table costruttore"
linktitle: "Table"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::Table costruttore. Inizializza una nuova istanza della classe Table in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Inizializza una nuova istanza della classe [Table](../).

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
## Note


Quando la [Table](../) viene creata, appartiene al documento specificato, ma non è ancora parte del documento e [ParentNode](../../../aspose.words/node/get_parentnode/) è **null**.

Per aggiungere la [Table](../) al documento usa [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) nella storia dove desideri inserire la tabella.

## Esempi



Mostra come creare una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Le tabelle contengono righe, che contengono celle, che possono avere paragrafi
// con elementi tipici come run, forme e persino altre tabelle.
// Chiamare il metodo "EnsureMinimum" su una tabella garantirà che
// la tabella abbia almeno una riga, una cella e un paragrafo.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Aggiungi testo alla prima cella nella prima riga della tabella.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## Vedi anche

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
