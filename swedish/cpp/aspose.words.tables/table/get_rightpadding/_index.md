---
title: "Aspose::Words::Tables::Table::get_RightPadding metod"
linktitle: "get_RightPadding"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_RightPadding metod. Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till höger om cellernas innehåll i C++."
type: docs
weight: 32000
url: /sv/cpp/aspose.words.tables/table/get_rightpadding/
---
## Table::get_RightPadding method


Hämtar eller anger mängden utrymme (i punkter) som ska läggas till höger om cellernas innehåll.

```cpp
double Aspose::Words::Tables::Table::get_RightPadding()
```


## Exempel



Visar hur man konfigurerar innehållspadding i en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// För varje cell i tabellen, ställ in avståndet mellan dess innehåll och var och en av dess kanter.
// Denna tabell kommer att upprätthålla det minsta paddingavståndet genom att radbryta text.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
