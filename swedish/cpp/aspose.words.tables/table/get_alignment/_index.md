---
title: "Aspose::Words::Tables::Table::get_Alignment metod"
linktitle: "get_Alignment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_Alignment metod. Anger hur en inbäddad tabell är justerad i dokumentet i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.tables/table/get_alignment/
---
## Table::get_Alignment method


Anger hur en inline‑tabell är justerad i dokumentet.

```cpp
Aspose::Words::Tables::TableAlignment Aspose::Words::Tables::Table::get_Alignment()
```

## Anmärkningar


Standardvärdet är [Left](../../tablealignment/).

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

* Enum [TableAlignment](../../tablealignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
