---
title: Aspose::Words::Tables::Table::get_AllowAutoFit method
linktitle: get_AllowAutoFit
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_AllowAutoFit method. Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Remarks


The default value is **true**.

## Examples



Shows how to enable/disable automatic table cell resizing. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Set the "AllowAutoFit" property to "false" to get the table to maintain the dimensions
// of all its rows and cells, and truncate contents if they get too large to fit.
// Set the "AllowAutoFit" property to "true" to allow the table to change its cells' width and height
// to accommodate their contents.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
