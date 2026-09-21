---
title: "Aspose::Words::Shading class"
linktitle: "Shading"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Shading class. Innehåller skuggningsegenskaper för ett objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 60000
url: /sv/cpp/aspose.words/shading/
---
## Shading class


Innehåller skuggningsattribut för ett objekt. För att lära dig mer, besök dokumentationsartikeln [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Tar bort skuggning från objektet. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Bestämmer om den angivna [Shading](./) är lika i värde med den aktuella [Shading](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Hämtar eller anger färgen som tillämpas på bakgrunden för [Shading](./)-objektet. |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Hämtar eller anger bakgrundsmönstrets temafärg i det tillämpade färgschemat som är associerat med detta [Shading](./)-objekt. |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en bakgrundstematisk färg. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Hämtar eller anger färgen som tillämpas på förgrunden för [Shading](./)-objektet. |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Hämtar eller anger förgrundsmönstrets temafärg i det tillämpade färgschemat som är associerat med detta [Shading](./)-objekt. |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en förgrundstematisk färg. |
| [get_Texture](./get_texture/)() | Hämtar eller anger skuggningens textur. |
| [GetHashCode](./gethashcode/)() const override | Fungerar som en hash-funktion för denna typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Sättare för [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Sättare för [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | Sättare för [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Sättare för [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Sättare för [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | Sättare för [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Sättare för [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man applicerar kant- och skuggningsfärg när man bygger en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Starta en tabell och ange en standardfärg/-tjocklek för dess kanter.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Skapa en rad med två celler med olika bakgrundsfärger.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Återställ cellformatering för att inaktivera bakgrundsfärgerna
// ange en anpassad kanttjocklek för alla nya celler som skapas av byggaren,
// bygg sedan en andra rad.
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


Visar hur man dekorerar text med kanter och skuggning.
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

## Se även

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
