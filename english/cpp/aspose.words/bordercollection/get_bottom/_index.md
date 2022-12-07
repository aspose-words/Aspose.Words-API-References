---
title: get_Bottom
second_title: Aspose.Words for C++ API Reference
description: Gets the bottom border.
type: docs
weight: 40
url: /cpp/aspose.words/bordercollection/get_bottom/
---
## BorderCollection::get_Bottom method


Gets the bottom border.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Bottom()
```


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

## See Also

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
