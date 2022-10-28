---
title: Shading
second_title: Aspose.Words for C++ API Reference
description: Contains shading attributes for an object.
type: docs
weight: 768
url: /cpp/aspose.words/shading/
---
## Shading class


Contains shading attributes for an object.

```cpp
class Shading : public Aspose::Words::InternableComplexAttr, public Aspose::Words::IComplexAttr
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Removes shading from the object. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Determines whether the specified [Shading](./) is equal in value to the current [Shading](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Gets or sets the color that's applied to the background of the [Shading](./) object. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Gets or sets the color that's applied to the foreground of the [Shading](./) object. |
| [get_Texture](./get_texture/)() | Gets or sets the shading texture. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Setter for [Aspose::Words::Shading::get_Texture](./get_texture/). |

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


Shows how to decorate text with borders and shading. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(BorderType::Left)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Right)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Top)->set_LineStyle(LineStyle::Double);
borders->idx_get(BorderType::Bottom)->set_LineStyle(LineStyle::Double);

SharedPtr<Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(ArtifactsDir + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

