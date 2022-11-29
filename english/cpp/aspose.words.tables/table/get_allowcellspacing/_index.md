---
title: get_AllowCellSpacing
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the "Allow spacing between cells" option.
type: docs
weight: 144
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
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

doc->Save(ArtifactsDir + u"Table.AllowCellSpacing.html");

// Adjusting the "CellSpacing" property will automatically enable cell spacing.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
