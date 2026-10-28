---
title: Aspose::Words::Tables::Table::set_RightPadding method
linktitle: set_RightPadding
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::set_RightPadding method. Sets the amount of space (in points) to add to the right of the contents of cells in C++.'
type: docs
weight: 125000
url: /cpp/aspose.words.tables/table/set_rightpadding/
---
## Table::set_RightPadding method


Sets the amount of space (in points) to add to the right of the contents of cells.

```cpp
void Aspose::Words::Tables::Table::set_RightPadding(double value)
```

## Examples


Shows how to configure content padding in a table.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// For every cell in the table, set the distance between its contents and each of its borders.
// This table will maintain the minimum padding distance by wrapping text.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```
## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
