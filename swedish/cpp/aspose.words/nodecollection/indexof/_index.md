---
title: "Aspose::Words::NodeCollection::IndexOf metod"
linktitle: "IndexOf"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::IndexOf‑metod. Returnerar det nollbaserade indexet för den angivna noden i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Returnerar det nollbaserade indexet för den angivna noden.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nod | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Noden att hitta. |

### ReturnValue

Det nollbaserade indexet för noden inom samlingen, om den hittas; annars -1.
## Anmärkningar


Denna metod utför en linjär sökning; därför är den genomsnittliga exekveringstiden proportionell mot [Count](../get_count/).

## Exempel



Visar hur man får indexet för en nod i en samling.
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

## Se även

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
