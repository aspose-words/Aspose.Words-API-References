---
title: SetBorders
second_title: Aspose.Words for C++ API Reference
description: Sets all table borders to the specified line style, width and color.
type: docs
weight: 846
url: /cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Sets all table borders to the specified line style, width and color.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | The line style to apply. |
| lineWidth | double | The line width to set (in points). |
| color | System::Drawing::Color | The color to use for the border. |

## Examples



Shows how to apply border and shading color while building a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Start a table and set a default color/thickness for its borders.
SharedPtr<Table> table = builder->StartTable();
table->SetBorders(LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Create a row with two cells with different background colors.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Reset cell formatting to disable the background colors
// set a custom border thickness for all new cells created by the builder,
// then build a second row.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(ArtifactsDir + u"DocumentBuilder.TableBordersAndShading.docx");
```


Shows how to format of all of a table's borders at once. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Clear all existing borders from the table.
table->ClearBorders();

// Set a single green line to serve as every outer and inner border of this table.
table->SetBorders(LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(ArtifactsDir + u"Table.SetBorders.docx");
```

## See Also

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
