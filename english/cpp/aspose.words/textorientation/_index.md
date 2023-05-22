---
title: Aspose::Words::TextOrientation enum
linktitle: TextOrientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextOrientation enum. Specifies orientation of text on a page, in a table cell or a text frame in C++.'
type: docs
weight: 124000
url: /cpp/aspose.words/textorientation/
---
## TextOrientation enum


Specifies orientation of text on a page, in a table cell or a text frame.

```cpp
enum class TextOrientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | 0 | Text is arranged horizontally (lr-tb). |
| Downward | 1 | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| Upward | 3 | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| HorizontalRotatedFarEast | 4 | Text is arranged horizontally, but Far East characters are rotated 90 degrees to the left (lr-tb-v). |
| VerticalFarEast | 5 | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VerticalRotatedFarEast | 7 | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally (tb-lr-v). |


## Examples



Shows how to build a formatted 2x2 table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
ASSERT_EQ(CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

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
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(ArtifactsDir + u"DocumentBuilder.BuildTable.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
