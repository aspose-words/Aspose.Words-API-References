---
title: Aspose::Words::Tables::Table::get_AllowCellSpacing method
linktitle: get_AllowCellSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_AllowCellSpacing method. Gets or sets the "Allow spacing between cells" option in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Gets or sets the "Allow spacing between cells" option.

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Examples



Shows how to enable spacing between individual cells in a table. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Set the "AllowCellSpacing" property to "true" to enable spacing between cells
// with a magnitude equal to the value of the "CellSpacing" property, in points.
// Set the "AllowCellSpacing" property to "false" to disable cell spacing
// and ignore the value of the "CellSpacing" property.
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Adjusting the "CellSpacing" property will automatically enable cell spacing.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
