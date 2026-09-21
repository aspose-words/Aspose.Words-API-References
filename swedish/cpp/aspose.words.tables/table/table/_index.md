---
title: "Aspose::Words::Tables::Table::Table konstruktor"
linktitle: "Table"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::Table konstruktor. Initierar en ny instans av Table‑klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Initierar en ny instans av klassen [Table](../).

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
## Anmärkningar


När [Table](../) skapas tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../../aspose.words/node/get_parentnode/) är **null**.

För att lägga till [Table](../) i dokumentet, använd [InsertAfter1()</see> eller <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) på den berättelse där du vill att tabellen infogas.

## Exempel



Visar hur man skapar en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tabeller innehåller rader, som innehåller celler, som kan ha stycken
// med typiska element som körningar, former och till och med andra tabeller.
// Att anropa metoden "EnsureMinimum" på en tabell kommer att säkerställa att
// tabellen har minst en rad, cell och stycke.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Lägg till text i den första cellen i den första raden i tabellen.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## Se även

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
