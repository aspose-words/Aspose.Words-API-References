---
title: Aspose::Words::Tables::Cell::EnsureMinimum method
linktitle: EnsureMinimum
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Cell::EnsureMinimum method. If the last child is not a paragraph, creates and appends one empty paragraph in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


If the last child is not a paragraph, creates and appends one empty paragraph.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Examples



Shows how to ensure a cell node contains the nodes we need to begin adding content to it. 
```cpp
auto doc = MakeObject<Document>();
auto table = MakeObject<Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild(table);
auto row = MakeObject<Row>(doc);
table->AppendChild(row);
auto cell = MakeObject<Cell>(doc);
row->AppendChild(cell);

// Cells may contain paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new cell does not have any paragraphs, and we cannot add contents such as run and shape nodes to it until it does.
ASSERT_EQ(0, cell->GetChildNodes(NodeType::Any, true)->get_Count());

// Calling the "EnsureMinimum" method on a cell will ensure that
// the cell has at least one empty paragraph, which we can then add contents to.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));
```

## See Also

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
