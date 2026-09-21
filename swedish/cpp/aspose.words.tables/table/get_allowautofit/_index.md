---
title: "Aspose::Words::Tables::Table::get_AllowAutoFit metod"
linktitle: "get_AllowAutoFit"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_AllowAutoFit metod. Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar innehållet i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar innehållet.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Anmärkningar


Standardvärdet är **true**.

## Exempel



Visar hur man aktiverar/inaktiverar automatisk storleksändring av tabellceller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Ställ in egenskapen "AllowAutoFit" till "false" för att få tabellen att behålla dimensionerna
// för alla dess rader och celler, och trunkera innehållet om det blir för stort för att få plats.
// Ställ in egenskapen "AllowAutoFit" till "true" för att låta tabellen ändra cellernas bredd och höjd
// för att rymma deras innehåll.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
