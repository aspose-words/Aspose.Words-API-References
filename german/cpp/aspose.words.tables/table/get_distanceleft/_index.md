---
title: "Aspose::Words::Tables::Table::get_DistanceLeft Methode"
linktitle: "get_DistanceLeft"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_DistanceLeft Methode. Ermittelt oder legt die Entfernung zwischen dem linken Rand der Tabelle und dem umgebenden Text fest, in Punkten in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words.tables/table/get_distanceleft/
---
## Table::get_DistanceLeft method


Liest oder legt den Abstand zwischen der linken Seite der Tabelle und dem umgebenden Text in Punkten fest.

```cpp
double Aspose::Words::Tables::Table::get_DistanceLeft()
```


## Beispiele



Zeigt, wie man den Abstand zwischen Tabellengrenzen und Text festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Abstand zwischen Tabelle und umgebendem Text festlegen.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
