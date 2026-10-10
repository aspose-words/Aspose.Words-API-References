---
title: "Aspose::Words::Tables::Table::AutoFit method"
linktitle: "AutoFit"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::AutoFit method. Ändrar storlek på tabellen och cellerna enligt det angivna auto‑fit‑beteendet i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


Ändrar storlek på tabellen och cellerna enligt det angivna auto‑fit‑beteendet.

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| behavior | Aspose::Words::Tables::AutoFitBehavior | Anger hur tabellen ska auto‑fitas. |
## Anmärkningar


Denna metod efterliknar kommandona som finns i Auto Fit‑menyn för en tabell i Microsoft Word. De tillgängliga kommandona är "Auto Fit to Contents", "Auto Fit to Window" och "Fixed Column Width". I Microsoft Word sätter dessa kommandon relevanta tabell‑egenskaper och uppdaterar sedan tabellens layout, och Aspose.Words gör samma sak åt dig.

## Exempel



Visar hur man bygger en ny tabell samtidigt som man tillämpar en stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Vi måste infoga minst en rad innan någon tabellformatering ställs in.
builder->InsertCell();

// Ange den tabellstil som ska användas baserat på stilidentifieraren.
// Observera att inte alla tabellstilar är tillgängliga när du sparar i .doc‑format.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Tillämpa stilen delvis på tabellens egenskaper baserat på predikat, och bygg sedan tabellen.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## Se även

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
