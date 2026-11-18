---
title: Aspose::Words::Tables::AutoFitBehavior enum
linktitle: AutoFitBehavior
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::AutoFitBehavior enum. Determines how Aspose.Words resizes the table when you invoke the AutoFit() method in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Determines how Aspose.Words resizes the table when you invoke the [AutoFit()](../table/autofit/) method.

```cpp
enum class AutoFitBehavior : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout.

In the resulting table, cell widths are updated to fit the table contents. Most likely, the table will shrink. |
| AutoFitToWindow | 1 | When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%, removes preferred widths from all cells and then updates the table layout.

As a result, the table occupies all available width and the cell widths are updated to fit table contents. |
| FixedColumnWidths | 2 | Aspose.Words disables the AutoFit option and removes the preferred with from the table.

The widths of the cells remain as they are specified by their [Width](../cellformat/get_width/) properties. |

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

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

Shows how to build a formatted 2x2 table.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
ASSERT_EQ(table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment(), CellVerticalAlignment::Center);
ASSERT_EQ(table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment(), CellVerticalAlignment::Center);

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
ASPOSE_ASSERT_EQ(table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height(), 0);
ASSERT_EQ(table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule(), HeightRule::Auto);
ASPOSE_ASSERT_EQ(table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height(), 100);
ASSERT_EQ(table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule(), HeightRule::Exactly);
ASSERT_EQ(table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation(), TextOrientation::Upward);
ASSERT_EQ(table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation(), TextOrientation::Downward);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```
## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
