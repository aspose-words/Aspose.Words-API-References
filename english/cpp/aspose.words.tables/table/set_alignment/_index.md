---
title: Aspose::Words::Tables::Table::set_Alignment method
linktitle: set_Alignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::set_Alignment method. Specifies how an inline table is aligned in the document in C++.'
type: docs
weight: 108000
url: /cpp/aspose.words.tables/table/set_alignment/
---
## Table::set_Alignment method


Specifies how an inline table is aligned in the document.

```cpp
void Aspose::Words::Tables::Table::set_Alignment(Aspose::Words::Tables::TableAlignment value)
```

## Remarks


The default value is [Left](../../tablealignment/).
## Examples


Shows how to apply an outline border to a table.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

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

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```
## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
