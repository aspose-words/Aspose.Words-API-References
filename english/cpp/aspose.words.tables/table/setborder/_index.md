---
title: Aspose::Words::Tables::Table::SetBorder method
linktitle: SetBorder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::SetBorder method. Sets the specified table border to the specified line style, width and color in C++.'
type: docs
weight: 68000
url: /cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


Sets the specified table border to the specified line style, width and color.

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| Parameter | Type | Description |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | The table border to change. |
| lineStyle | Aspose::Words::LineStyle | The line style to apply. |
| lineWidth | double | The line width to set (in points). |
| color | System::Drawing::Color | The color to use for the border. |
| isOverrideCellBorders | bool | When **true**, causes all existing explicit cell borders to be removed. |

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

## See Also

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
