---
title: Aspose::Words::Tables::CellVerticalAlignment enum
linktitle: CellVerticalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellVerticalAlignment enum. Specifies vertical justification of text inside a table cell in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enum


Specifies vertical justification of text inside a table cell.

```cpp
enum class CellVerticalAlignment : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Bottom | 2 | Text is aligned at the bottom of the cell. |
| Center | 1 | Text is aligned in the middle of a cell. |
| Top | 0 | Text is aligned at the top of a cell. |

## Examples


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
