---
title: TableStyleOptions
second_title: Aspose.Words for C++ API Reference
description: Specifies how table style is applied to a table.
type: docs
weight: 183
url: /cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Specifies how table style is applied to a table.

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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<Table> table = builder->StartTable();

// We must insert at least one row before setting any table formatting.
builder->InsertCell();

// Set the table style used based on the style identifier.
// Note that not all table styles are available when saving to .doc format.
table->set_StyleIdentifier(StyleIdentifier::MediumShading1Accent1);

// Partially apply the style to features of the table based on predicates, then build the table.
table->set_StyleOptions(TableStyleOptions::FirstColumn | TableStyleOptions::RowBands | TableStyleOptions::FirstRow);
table->AutoFit(AutoFitBehavior::AutoFitToContents);

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

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertTableWithStyle.docx");
```

