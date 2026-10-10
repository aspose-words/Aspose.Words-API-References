---
title: "Aspose::Words::Tables::CellFormat::get_PreferredWidth‑metod"
linktitle: "get_PreferredWidth"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellFormat::get_PreferredWidth‑metod. Returnerar eller anger den föredragna bredden på cellen i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Returnerar eller anger den föredragna bredden för cellen.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Anmärkningar


Den föredragna bredden (tillsammans med tabellens Auto Fit‑alternativ) bestämmer hur den faktiska bredden på cellen beräknas av tabellens layout‑algoritm. [Table](../../table/) layout kan utföras av Aspose.Words när den sparar dokumentet eller av Microsoft Word när den visar dokumentet.

Den föredragna bredden kan anges i punkter eller i procent. Den föredragna bredden kan också anges som "auto", vilket betyder att ingen föredragen bredd är specificerad.

Standardvärdet är [Auto](../../preferredwidth/auto/).

## Exempel



Visar hur man anger en föredragen bredd för tabellceller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Det finns två sätt att tillämpa klassen "PreferredWidth" på tabellceller.
// 1 -  Ställ in en absolut föredragen bredd baserad på punkter:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Ställ in en relativ föredragen bredd baserad på procent av tabellens bredd:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// En cell utan angiven föredragen bredd kommer att ta upp resten av det tillgängliga utrymmet.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Varje konfiguration av egenskapen "PreferredWidth" skapar ett nytt objekt.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Se även

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
