---
title: "Aspose::Words::Tables::Cell::EnsureMinimum Methode"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Cell::EnsureMinimum Methode. Wenn das letzte Kind kein Absatz ist, erstellt und fügt sie in C++ einen leeren Absatz hinzu."
type: docs
weight: 4000
url: /de/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Wenn das letzte Kind kein Absatz ist, wird ein leerer Absatz erstellt und angehängt.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Beispiele



Zeigt, wie man sicherstellt, dass ein Zellen‑Knoten die Knoten enthält, die wir benötigen, um Inhalte hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Zellen können Absätze mit typischen Elementen wie Runs, Shapes und sogar anderen Tabellen enthalten.
// Unsere neue Zelle hat noch keine Absätze, und wir können keine Inhalte wie Run‑ und Shape‑Knoten hinzufügen, bis sie welche hat.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Der Aufruf der "EnsureMinimum"‑Methode auf einer Zelle stellt sicher, dass
// die Zelle mindestens einen leeren Absatz hat, zu dem wir dann Inhalte hinzufügen können.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Siehe auch

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
