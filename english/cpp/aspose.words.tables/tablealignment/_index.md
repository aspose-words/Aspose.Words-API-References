---
title: Aspose::Words::Tables::TableAlignment enum
linktitle: TableAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::TableAlignment enum. Specifies alignment for an inline table in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


Specifies alignment for an inline table.

```cpp
enum class TableAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | 0 | The table is aligned to the left. |
| Center | 1 | The table is centered. |
| Right | 2 | The table is aligned to the right. |


## Examples



Shows how to apply an outline border to a table. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Align the table to the center of the page.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Clear any existing borders and shading from the table.
table->ClearBorders();
table->ClearShading();

// Add green borders to the outline of the table.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Fill the cells with a light green solid color.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
