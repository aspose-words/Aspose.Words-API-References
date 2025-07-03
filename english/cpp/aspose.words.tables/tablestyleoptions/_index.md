---
title: Aspose::Words::Tables::TableStyleOptions enum
linktitle: TableStyleOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::TableStyleOptions enum. Specifies how table style is applied to a table in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Specifies how table style is applied to a table.

```cpp
enum class TableStyleOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No table style formatting is applied. |
| FirstRow | 32 | Apply first row conditional formatting. |
| LastRow | 64 | Apply last row conditional formatting. |
| FirstColumn | 128 | Apply 1 first column conditional formatting. |
| LastColumn | 256 | Apply last column conditional formatting. |
| RowBands | 512 | Apply row banding conditional formatting. |
| ColumnBands | 1024 | Apply column banding conditional formatting. |
| Default2003 | n/a | [Row](../row/) and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF. |
| Default | n/a | This is Microsoft Word defaults. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
