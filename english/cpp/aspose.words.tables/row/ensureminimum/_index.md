---
title: Aspose::Words::Tables::Row::EnsureMinimum method
linktitle: EnsureMinimum
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Row::EnsureMinimum method. If the Row has no cells, creates and appends one Cell in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


If the [Row](../) has no cells, creates and appends one [Cell](../../cell/).

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Examples



Shows how to ensure a row node contains the nodes we need to begin adding content to it. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Rows contain cells, containing paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new row has none of these nodes, and we cannot add contents to it until it does.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one cell with an empty paragraph.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## See Also

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
