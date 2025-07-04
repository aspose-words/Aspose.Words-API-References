---
title: Aspose::Words::NodeCollection::IndexOf method
linktitle: IndexOf
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::IndexOf method. Returns the zero-based index of the specified node in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Returns the zero-based index of the specified node.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Type | Description |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to locate. |

### ReturnValue

The zero-based index of the node within the collection, if found; otherwise, -1.
## Remarks


This method performs a linear search; therefore, the average execution time is proportional to [Count](../get_count/).

## Examples



Shows how to get the index of a node in a collection. 
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

## See Also

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
