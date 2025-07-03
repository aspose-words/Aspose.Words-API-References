---
title: Aspose::Words::Tables::Table::get_PreferredWidth method
linktitle: get_PreferredWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_PreferredWidth method. Gets or sets the table preferred width in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Gets or sets the table preferred width.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Remarks


The default value is [Auto](../../preferredwidth/auto/).

## Examples



Shows how to set a table to auto fit to 50% of the width of the page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## See Also

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
