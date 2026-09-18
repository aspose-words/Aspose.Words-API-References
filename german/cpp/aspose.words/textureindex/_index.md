---
title: "Aspose::Words::TextureIndex Enum"
linktitle: "TextureIndex"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextureIndex Enum. Gibt die Schattierungstextur in C++ an."
type: docs
weight: 125000
url: /de/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Gibt die Schattierungstextur an.

```cpp
enum class TextureIndex
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Textur22Pt5Prozent | 40 |  |
| Textur25Prozent | 5 |  |
| Textur27Pt5Prozent | 41 |  |
| Textur2Pt5Prozent | 35 |  |
| Textur30Prozent | 6 |  |
| Textur32Pt5Prozent | 42 |  |
| Textur35Prozent | 43 |  |
| Textur37Pt5Prozent | 44 |  |
| Textur40Prozent | 7 |  |
| Textur42Pt5Prozent | 45 |  |
| Textur45Prozent | 46 |  |
| Textur47Pt5Prozent | 47 |  |
| Textur50Prozent | 8 |  |
| Textur52Pt5Prozent | 48 |  |
| Textur55Prozent | 49 |  |
| Textur57Pt5Prozent | 50 |  |
| Textur5Prozent | 2 |  |
| Textur60Prozent | 9 |  |
| Textur62Pt5Prozent | 51 |  |
| Textur65Prozent | 52 |  |
| Textur67Pt5Prozent | 53 |  |
| Textur70Prozent | 10 |  |
| Textur72Pt5Prozent | 54 |  |
| Textur75Prozent | 11 |  |
| Textur77Pt5Prozent | 55 |  |
| Textur7Pt5Prozent | 36 |  |
| Textur80Prozent | 12 |  |
| Textur82Pt5Prozent | 56 |  |
| Textur85Prozent | 57 |  |
| Textur87Pt5Prozent | 58 |  |
| Textur90Prozent | 13 |  |
| Textur92Pt5Prozent | 59 |  |
| Textur95Prozent | 60 |  |
| Textur97Pt5Prozent | 61 |  |
| TexturKreuz | 24 |  |
| TexturDunkelKreuz | 18 |  |
| TexturDunkelDiagonalKreuz | 19 |  |
| TexturDunkelDiagonalRunter | 16 |  |
| TexturDunkelDiagonalHoch | 17 |  |
| TexturDunkelHorizontal | 14 |  |
| TexturDunkelVertikal | 15 |  |
| TexturDiagonalKreuz | 25 |  |
| TexturDiagonalRunter | 22 |  |
| TexturDiagonalHoch | 23 |  |
| TexturHorizontal | 20 |  |
| TexturKeine | 0 |  |
| TexturFest | 1 |  |
| TexturVertikal | 21 |  |
| TexturNull | 65535 | Gibt an, dass im aktuellen schattierten Bereich kein Muster verwendet werden darf (d. h. das Muster muss eine vollständige Füllung mit der Hintergrundfarbe sein). |


## Beispiele



Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.
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


Zeigt, wie man einer Tabelle einen Umrandungsrahmen hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Richtet die Tabelle zentriert auf der Seite aus.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Entfernt alle vorhandenen Rahmen und Schattierungen aus der Tabelle.
table->ClearBorders();
table->ClearShading();

// Fügt der Umrandung der Tabelle grüne Rahmen hinzu.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Füllt die Zellen mit einer hellgrünen Vollfarbe.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
