---
title: Aspose::Words::DocumentBuilder::EndRow method
linktitle: EndRow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::EndRow method. Ends a table row in the document in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/documentbuilder/endrow/
---
## DocumentBuilder::EndRow method


Ends a table row in the document.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::EndRow()
```


### ReturnValue

The row node that was just finished.
## Remarks


Call [EndRow](./) to end a table row. If you call [InsertCell](../insertcell/) immediately after that, then the table continues on a new row.

Use the [RowFormat](../get_rowformat/) property to specify row formatting.

## Examples



Shows how to merge table cells vertically. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of vertically merged cells.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::First);
builder->Write(u"Text in merged cells.");

// Insert a cell into the second column of the first row, then end the row.
// Also, configure the builder to disable vertical merging in created cells.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Insert a cell into the first column of the second row.
// Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::Previous);

// Insert another independent cell in the second column of the second row.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(ArtifactsDir + u"CellFormat.VerticalMerge.docx");
```


Shows how to build a table with custom borders. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->StartTable();

// Setting table formatting options for a document builder
// will apply them to every row and cell that we add with it.
builder->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Changing the formatting will apply it to the current cell,
// and any new cells that we create with the builder afterward.
// This will not affect the cells that we have added previously.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Increase row height to fit the vertical text.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertTable.docx");
```


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

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
