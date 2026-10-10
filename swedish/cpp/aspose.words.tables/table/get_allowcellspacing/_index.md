---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing metod"
linktitle: "get_AllowCellSpacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing metod. Hämtar eller anger alternativet \"Allow spacing between cells\" i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Hämtar eller anger alternativet "Allow spacing between cells".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Exempel



Visar hur man aktiverar avstånd mellan enskilda celler i en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Ställ in egenskapen "AllowCellSpacing" till "true" för att aktivera avstånd mellan celler
// med en storlek lika med värdet på egenskapen "CellSpacing", i punkter.
// Ställ in egenskapen "AllowCellSpacing" till "false" för att inaktivera cellavstånd
// och ignorera värdet på egenskapen "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Att justera egenskapen "CellSpacing" kommer automatiskt att aktivera cellavstånd.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
