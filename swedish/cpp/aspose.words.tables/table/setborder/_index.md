---
title: "Aspose::Words::Tables::Table::SetBorder-metoden"
linktitle: "SetBorder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::SetBorder-metoden. Ställer in den angivna tabellramen till den angivna linjestilen, bredden och färgen i C++."
type: docs
weight: 68000
url: /sv/cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


Sätter den angivna tabellramen till den angivna linjestilen, bredden och färgen.

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | Tabellramen att ändra. |
| lineStyle | Aspose::Words::LineStyle | Linjestilen att tillämpa. |
| lineWidth | double | Linjebredden att ange (i punkter). |
| color | System::Drawing::Color | Färgen att använda för ramen. |
| isOverrideCellBorders | bool | När **true**, tas alla befintliga explicita cellramar bort. |

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

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
