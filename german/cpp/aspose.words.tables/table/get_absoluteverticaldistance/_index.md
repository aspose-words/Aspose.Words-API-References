---
title: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance-Methode"
linktitle: "get_AbsoluteVerticalDistance"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance-Methode. Ruft die absolute vertikale Position einer schwebenden Tabelle ab oder legt sie fest, die durch die Tabelleneigenschaften in Punkt angegeben wird. Der Standardwert ist 0 in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.tables/table/get_absoluteverticaldistance/
---
## Table::get_AbsoluteVerticalDistance method


Liest oder setzt die absolute vertikale Position der schwebenden Tabelle, angegeben durch die Tabelleneigenschaften, in Punkten. Der Standardwert ist 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance()
```


## Beispiele



Zeigt, wie man den Standort schwebender Tabellen festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Setzen Sie den Standort der Tabelle an eine Stelle auf der Seite, zum Beispiel in diesem Fall die untere rechte Ecke.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Wir können auch einen horizontalen und vertikalen Versatz in Punkten von der Position des Absatzes, an dem wir die Tabelle eingefügt haben, festlegen.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
