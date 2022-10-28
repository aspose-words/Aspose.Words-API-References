---
title: get_AllowAutoFit
second_title: Aspose.Words for C++ API Reference
description: Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.
type: docs
weight: 131
url: /cpp/aspose.words.tables/table/get_allowautofit/
---
## Table.get_AllowAutoFit method


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```


The default value is **true**.

## Examples




Shows how to enable/disable automatic table cell resizing. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(PreferredWidth::FromPoints(100));
builder->Write(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
               u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(PreferredWidth::Auto());
builder->Write(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
               u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Set the "AllowAutoFit" property to "false" to get the table to maintain the dimensions
// of all its rows and cells, and truncate contents if they get too large to fit.
// Set the "AllowAutoFit" property to "true" to allow the table to change its cells' width and height
// to accommodate their contents.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(ArtifactsDir + u"Table.AllowAutoFitOnTable.html");
```

