---
title: Aspose::Words::Tables::Table::get_StyleIdentifier method
linktitle: get_StyleIdentifier
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_StyleIdentifier method. Gets or sets the locale independent style identifier of the table style applied to this table in C++.'
type: docs
weight: 35000
url: /cpp/aspose.words.tables/table/get_styleidentifier/
---
## Table::get_StyleIdentifier method


Gets or sets the locale independent style identifier of the table style applied to this table.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Tables::Table::get_StyleIdentifier()
```


## Examples



Shows how to build a new table while applying a style. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// We must insert at least one row before setting any table formatting.
builder->InsertCell();

// Set the table style used based on the style identifier.
// Note that not all table styles are available when saving to .doc format.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Partially apply the style to features of the table based on predicates, then build the table.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## See Also

* Enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
