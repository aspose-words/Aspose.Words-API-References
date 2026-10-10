---
title: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance metod"
linktitle: "get_AbsoluteVerticalDistance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance metod. Hämtar eller anger absolut vertikal flytande tabellposition som specificeras av tabellens egenskaper, i punkter. Standardvärdet är 0 i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.tables/table/get_absoluteverticaldistance/
---
## Table::get_AbsoluteVerticalDistance method


Hämtar eller anger absolut vertikal flytande tabellposition som specificeras av tabellens egenskaper, i punkter. Standardvärdet är 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance()
```


## Exempel



Visar hur man ställer in platsen för flytande tabeller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Ställ in tabellens plats på sidan, till exempel i det här fallet i det nedre högra hörnet.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Vi kan också ange ett horisontellt och vertikalt avstånd i punkter från styckets plats där vi infogade tabellen.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
