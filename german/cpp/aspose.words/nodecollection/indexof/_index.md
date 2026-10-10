---
title: "Aspose::Words::NodeCollection::IndexOf-Methode"
linktitle: "IndexOf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeCollection::IndexOf-Methode. Gibt den nullbasierten Index des angegebenen Knotens in C++ zurück."
type: docs
weight: 9000
url: /de/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Gibt den nullbasierten Index des angegebenen Knotens zurück.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Knoten | const System::SharedPtr\<Aspose::Words::Node\>\& | Der zu findende Knoten. |

### ReturnValue

Der nullbasierte Index des Knotens innerhalb der Sammlung, falls gefunden; andernfalls -1.
## Hinweise


Diese Methode führt eine lineare Suche durch; daher ist die durchschnittliche Ausführungszeit proportional zu [Count](../get_count/).

## Beispiele



Zeigt, wie man den Index eines Knotens in einer Sammlung erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## Siehe auch

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
