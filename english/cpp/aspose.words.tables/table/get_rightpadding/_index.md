---
title: get_RightPadding
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the amount of space (in points) to add to the right of the contents of cells.
type: docs
weight: 404
url: /cpp/aspose.words.tables/table/get_rightpadding/
---
## Table::get_RightPadding method


Gets or sets the amount of space (in points) to add to the right of the contents of cells.

```cpp
double Aspose::Words::Tables::Table::get_RightPadding()
```


## Examples



Shows how to configure content padding in a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
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

doc->Save(ArtifactsDir + u"DocumentBuilder.SetRowFormatting.docx");
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
