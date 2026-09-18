---
title: "Aspose::Words::Tables::Row::EnsureMinimum Methode"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Row::EnsureMinimum Methode. Wenn die Row keine Zellen hat, wird in C++ eine Cell erstellt und angehängt."
type: docs
weight: 4000
url: /de/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Wenn die [Row](../) keine Zellen hat, wird eine [Cell](../../cell/) erstellt und angehängt.

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Beispiele



Zeigt, wie man sicherstellt, dass ein Row-Knoten die Knoten enthält, die wir benötigen, um Inhalte hinzuzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Rows enthalten Zellen, die Absätze mit typischen Elementen wie Runs, Shapes und sogar anderen Tabellen enthalten.
// Unsere neue Row hat keinen dieser Knoten, und wir können keine Inhalte hinzufügen, bis sie vorhanden sind.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Der Aufruf der Methode "EnsureMinimum" an einer Tabelle stellt sicher, dass
// Die Tabelle hat mindestens eine Zelle mit einem leeren Absatz.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Siehe auch

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
