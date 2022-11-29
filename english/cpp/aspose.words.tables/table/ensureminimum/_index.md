---
title: EnsureMinimum
second_title: Aspose.Words for C++ API Reference
description: If the table has no rows, creates and appends one Row.
type: docs
weight: 79
url: /cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


If the table has no rows, creates and appends one **Row**.

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Examples



Shows how to ensure that a table node contains the nodes we need to add content. 
```cpp
auto doc = MakeObject<Document>();
auto table = MakeObject<Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild(table);

// Tables contain rows, which contain cells, which may contain paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Our new table has none of these nodes, and we cannot add contents to it until it does.
ASSERT_EQ(0, table->GetChildNodes(NodeType::Any, true)->get_Count());

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row and one cell with an empty paragraph.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
