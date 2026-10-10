---
title: "Aspose::Words::Tables::Table::Table-Konstruktor"
linktitle: "Table"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::Table-Konstruktor. Initialisiert eine neue Instanz der Table‑Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Initialisiert eine neue Instanz der [Table](../)-Klasse.

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
## Hinweise


Wenn [Table](../) erstellt wird, gehört sie zum angegebenen Dokument, ist jedoch noch kein Teil des Dokuments und [ParentNode](../../../aspose.words/node/get_parentnode/) ist **null**.

Um [Table](../) an das Dokument anzuhängen, verwenden Sie [InsertAfter1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) in der Story, in der Sie die Tabelle einfügen möchten.

## Beispiele



Zeigt, wie man eine Tabelle erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze haben können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Der Aufruf der Methode "EnsureMinimum" an einer Tabelle stellt sicher, dass
// die Tabelle mindestens eine Zeile, Zelle und einen Absatz hat.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Fügen Sie Text zur ersten Zelle in der ersten Zeile der Tabelle hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## Siehe auch

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
