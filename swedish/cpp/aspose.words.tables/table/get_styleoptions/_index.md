---
title: "Aspose::Words::Tables::Table::get_StyleOptions‑metod"
linktitle: "get_StyleOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_StyleOptions‑metod. Hämtar eller anger bitflaggor som specificerar hur en tabellstil tillämpas på den här tabellen i C++."
type: docs
weight: 37000
url: /sv/cpp/aspose.words.tables/table/get_styleoptions/
---
## Table::get_StyleOptions method


Hämtar eller anger bitflaggor som specificerar hur en tabellstil tillämpas på denna tabell.

```cpp
Aspose::Words::Tables::TableStyleOptions Aspose::Words::Tables::Table::get_StyleOptions()
```


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

* Enum [TableStyleOptions](../../tablestyleoptions/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
