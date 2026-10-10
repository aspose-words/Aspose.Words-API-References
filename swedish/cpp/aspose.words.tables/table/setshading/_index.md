---
title: "Aspose::Words::Tables::Table::SetShading metod"
linktitle: "SetShading"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::SetShading metod. Ställer in skuggning till de angivna värdena på hela tabellen i C++."
type: docs
weight: 70000
url: /sv/cpp/aspose.words.tables/table/setshading/
---
## Table::SetShading method


Ställer in skuggning till de angivna värdena på hela tabellen.

```cpp
void Aspose::Words::Tables::Table::SetShading(Aspose::Words::TextureIndex texture, System::Drawing::Color foregroundColor, System::Drawing::Color backgroundColor)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| textur | Aspose::Words::TextureIndex | Texturen att använda. |
| foregroundColor | System::Drawing::Color | Färgen på texturen. |
| backgroundColor | System::Drawing::Color | Färgen på bakgrundsfyllningen. |

## Exempel



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

* Enum [TextureIndex](../../../aspose.words/textureindex/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
