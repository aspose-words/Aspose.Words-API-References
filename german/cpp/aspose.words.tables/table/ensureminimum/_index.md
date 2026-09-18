---
title: "Aspose::Words::Tables::Table::EnsureMinimum Methode"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::EnsureMinimum Methode. Wenn die Tabelle keine Zeilen hat, wird in C++ eine Zeile erstellt und angehängt."
type: docs
weight: 8000
url: /de/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Wenn die Tabelle keine Zeilen hat, wird eine [Row](../../row/) erstellt und angehängt.

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Beispiele



Zeigt, wie man sicherstellt, dass ein Tabellenknoten die Knoten enthält, die wir zum Hinzufügen von Inhalten benötigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die wiederum Absätze enthalten können.
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Unsere neue Tabelle hat keinen dieser Knoten, und wir können ihr keine Inhalte hinzufügen, bis sie diese hat.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Der Aufruf der Methode "EnsureMinimum" an einer Tabelle stellt sicher, dass
// Die Tabelle hat mindestens eine Zeile und eine Zelle mit einem leeren Absatz.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
