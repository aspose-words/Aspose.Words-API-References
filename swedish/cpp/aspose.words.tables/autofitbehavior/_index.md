---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::AutoFitBehavior enum. Bestämmer hur Aspose.Words ändrar storlek på tabellen när du anropar AutoFit()-metoden i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Bestämmer hur Aspose.Words ändrar storlek på tabellen när du anropar [AutoFit()](../table/autofit/) metoden.

```cpp
enum class AutoFitBehavior
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words aktiverar AutoFit-alternativet, tar bort den föredragna bredden från tabellen och alla celler och uppdaterar sedan tabellens layout. I den resulterande tabellen uppdateras cellbredderna så att de passar tabellens innehåll. Troligen kommer tabellen att krympa. |
| AutoFitToWindow | 1 | När du använder detta värde aktiverar Aspose.Words AutoFit‑alternativet, sätter den föredragna bredden för tabellen till 100 %, tar bort föredragna bredder från alla celler och uppdaterar sedan tabellens layout. Som ett resultat fyller tabellen hela den tillgängliga bredden och cellbredderna uppdateras för att passa tabellens innehåll. |
| FixedColumnWidths | 2 | Aspose.Words inaktiverar AutoFit‑alternativet och tar bort den föredragna bredden från tabellen. Cellernas bredder förblir som de är angivna av deras [Width](../cellformat/get_width/)‑egenskaper. |


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


Visar hur man bygger en formaterad 2x2-tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// När tabellen byggs kommer dokumentbyggaren att tillämpa sina aktuella RowFormat/CellFormat-egenskapsvärden.
// på den aktuella rad/cell som dess markör befinner sig i och på alla nya rader/celler när den skapar dem.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Tidigare tillagda rader och celler påverkas inte retroaktivt av förändringar i byggarens formatering.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Se även

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
