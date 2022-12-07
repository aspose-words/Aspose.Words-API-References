---
title: get_PreferredWidth
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the table preferred width.
type: docs
weight: 365
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(PreferredWidth::FromPercent(50));

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## See Also

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
