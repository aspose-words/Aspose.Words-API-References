---
title: EnsureMinimum
second_title: Aspose.Words for C++ API Reference
description: If the Row has no cells, creates and appends one Cell.
type: docs
weight: 27
url: /cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


If the **Row** has no cells, creates and appends one **Cell**.

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Examples



Shows how to ensure a row node contains the nodes we need to begin adding content to it. 
```cpp
auto doc = MakeObject<Document>();
auto table = MakeObject<Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild(table);
auto row = MakeObject<Row>(doc);
table->AppendChild(row);

// Rows contain cells, containing paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new row has none of these nodes, and we cannot add contents to it until it does.
ASSERT_EQ(0, row->GetChildNodes(NodeType::Any, true)->get_Count());

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one cell with an empty paragraph.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));
```

## See Also

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
