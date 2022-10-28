---
title: ClearBorders
second_title: Aspose.Words for C++ API Reference
description: Removes all table and cell borders on this table.
type: docs
weight: 40
url: /cpp/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method


Removes all table and cell borders on this table.

```cpp
void Aspose::Words::Tables::Table::ClearBorders()
```


## Examples




Shows how to apply an outline border to a table. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Align the table to the center of the page.
table->set_Alignment(TableAlignment::Center);

// Clear any existing borders and shading from the table.
table->ClearBorders();
table->ClearShading();

// Add green borders to the outline of the table.
table->SetBorder(BorderType::Left, LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(BorderType::Right, LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(BorderType::Top, LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(BorderType::Bottom, LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Fill the cells with a light green solid color.
table->SetShading(TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(ArtifactsDir + u"Table.SetOutlineBorders.docx");
```


Shows how to remove all borders from a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

// Modify the color and thickness of the top border.
SharedPtr<Border> topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(BorderType::Top);
table->SetBorder(BorderType::Top, LineStyle::Double, 1.5, System::Drawing::Color::get_Red(), true);

ASPOSE_ASSERT_EQ(1.5, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(LineStyle::Double, topBorder->get_LineStyle());

// Clear the borders of all cells in the table, and then save the document.
table->ClearBorders();
doc->Save(ArtifactsDir + u"Table.ClearBorders.docx");

// Verify the values of the table's properties after re-opening the document.
doc = MakeObject<Document>(ArtifactsDir + u"Table.ClearBorders.docx");
table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(BorderType::Top);

ASPOSE_ASSERT_EQ(0.0, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(LineStyle::None, topBorder->get_LineStyle());
```

