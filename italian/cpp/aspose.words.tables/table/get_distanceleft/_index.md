---
title: "Aspose::Words::Tables::Table::get_DistanceLeft metodo"
linktitle: "get_DistanceLeft"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_DistanceLeft metodo. Ottiene o imposta la distanza tra il lato sinistro della tabella e il testo circostante, in punti in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.tables/table/get_distanceleft/
---
## Table::get_DistanceLeft method


Ottiene o imposta la distanza tra il lato sinistro della tabella e il testo circostante, in punti.

```cpp
double Aspose::Words::Tables::Table::get_DistanceLeft()
```


## Esempi



Mostra come impostare la distanza tra i bordi della tabella e il testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Imposta la distanza tra la tabella e il testo circostante.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
