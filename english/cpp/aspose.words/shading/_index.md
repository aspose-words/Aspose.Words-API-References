---
title: Aspose::Words::Shading class
linktitle: Shading
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Shading class. Contains shading attributes for an object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 60000
url: /cpp/aspose.words/shading/
---
## Shading class


Contains shading attributes for an object. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Removes shading from the object. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Determines whether the specified [Shading](./) is equal in value to the current [Shading](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Gets or sets the color that's applied to the background of the [Shading](./) object. |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Gets or sets the background pattern theme color in the applied color scheme that is associated with this [Shading](./) object. |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Gets or sets a double value that lightens or darkens a background theme color. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Gets or sets the color that's applied to the foreground of the [Shading](./) object. |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Gets or sets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](./) object. |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Gets or sets a double value that lightens or darkens a foreground theme color. |
| [get_Texture](./get_texture/)() | Gets or sets the shading texture. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter for [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | Setter for [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter for [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | Setter for [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Setter for [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## Examples



Shows how to apply border and shading color while building a table. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Start a table and set a default color/thickness for its borders.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

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

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Shows how to decorate text with borders and shading. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## See Also

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
