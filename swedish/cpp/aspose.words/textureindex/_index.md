---
title: "Aspose::Words::TextureIndex-enum"
linktitle: "TextureIndex"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextureIndex-enum. Anger skuggningstextur i C++."
type: docs
weight: 125000
url: /sv/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Anger skuggningstextur.

```cpp
enum class TextureIndex
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Texture22Pt5Percent | 40 |  |
| Texture25Percent | 5 |  |
| Texture27Pt5Percent | 41 |  |
| Textur2Pt5Procent | 35 |  |
| Textur30Procent | 6 |  |
| Textur32Pt5Procent | 42 |  |
| Textur35Procent | 43 |  |
| Textur37Pt5Procent | 44 |  |
| Textur40Procent | 7 |  |
| Textur42Pt5Procent | 45 |  |
| Textur45Procent | 46 |  |
| Textur47Pt5Procent | 47 |  |
| Textur50Procent | 8 |  |
| Textur52Pt5Procent | 48 |  |
| Textur55Procent | 49 |  |
| Textur57Pt5Procent | 50 |  |
| Textur5Procent | 2 |  |
| Textur60Procent | 9 |  |
| Textur62Pt5Procent | 51 |  |
| Textur65Procent | 52 |  |
| Textur67Pt5Procent | 53 |  |
| Textur70Procent | 10 |  |
| Textur72Pt5Procent | 54 |  |
| Textur75Procent | 11 |  |
| Textur77Pt5Procent | 55 |  |
| Textur7Pt5Procent | 36 |  |
| Textur80Procent | 12 |  |
| Textur82Pt5Procent | 56 |  |
| Texture85Percent | 57 |  |
| Texture87Pt5Percent | 58 |  |
| Texture90Percent | 13 |  |
| Texture92Pt5Percent | 59 |  |
| Texture95Percent | 60 |  |
| Texture97Pt5Percent | 61 |  |
| TextureCross | 24 |  |
| TextureDarkCross | 18 |  |
| TextureDarkDiagonalCross | 19 |  |
| TextureDarkDiagonalDown | 16 |  |
| TextureDarkDiagonalUp | 17 |  |
| TextureDarkHorizontal | 14 |  |
| TextureDarkVertical | 15 |  |
| TextureDiagonalCross | 25 |  |
| TextureDiagonalDown | 22 |  |
| TextureDiagonalUp | 23 |  |
| TextureHorizontal | 20 |  |
| TextureNone | 0 |  |
| TextureSolid | 1 |  |
| TextureVertical | 21 |  |
| TextureNil | 65535 | Anger att ingen mönster ska användas i det aktuella skuggade området (dvs. att mönstret ska vara en komplett fyllning med bakgrundsfärgen). |


## Exempel



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


Visar hur man applicerar en konturram på en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Justera tabellen till sidans centrum.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Rensa eventuella befintliga kanter och skuggning från tabellen.
table->ClearBorders();
table->ClearShading();

// Lägg till gröna kanter runt tabellens kontur.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Fyll cellerna med en ljusgrön solid färg.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
