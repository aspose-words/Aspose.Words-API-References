---
title: IndexOf
second_title: Aspose.Words for C++ API Reference
description: Returns the zero-based index of the specified node.
type: docs
weight: 79
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


This method performs a linear search; therefore, the average execution time is proportional to Count.

## Examples



Shows how to get the index of a node in a collection. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
SharedPtr<NodeCollection> allTables = doc->GetChildNodes(NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

SharedPtr<Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

SharedPtr<Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## See Also

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
