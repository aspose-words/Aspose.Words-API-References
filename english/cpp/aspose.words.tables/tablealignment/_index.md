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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
