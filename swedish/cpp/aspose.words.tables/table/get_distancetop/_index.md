---
title: "Aspose::Words::Tables::Table::get_DistanceTop metod"
linktitle: "get_DistanceTop"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_DistanceTop metod. Hämtar eller anger avståndet mellan tabellens överkant och den omgivande texten, i punkter i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.tables/table/get_distancetop/
---
## Table::get_DistanceTop method


Hämtar eller anger avståndet mellan tabellens topp och den omgivande texten, i punkter.

```cpp
double Aspose::Words::Tables::Table::get_DistanceTop()
```


## Exempel



Visar hur man ställer in avståndet mellan tabellens gränser och texten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Ställ in avståndet mellan tabellen och omgivande text.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
