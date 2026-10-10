---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing Methode"
linktitle: "get_AllowCellSpacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing-Methode. Ruft die Option \"Abstand zwischen Zellen zulassen\" ab oder legt sie fest in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Liest oder setzt die Option "Allow spacing between cells".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Beispiele



Zeigt, wie man den Abstand zwischen einzelnen Zellen in einer Tabelle aktiviert.
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

// Setzen Sie die Eigenschaft "AllowCellSpacing" auf "true", um den Abstand zwischen Zellen zu aktivieren.
// mit einer Größe, die dem Wert der Eigenschaft "CellSpacing" entspricht, in Punkten.
// Setzen Sie die Eigenschaft "AllowCellSpacing" auf "false", um den Zellenabstand zu deaktivieren.
// und ignorieren Sie den Wert der Eigenschaft "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Das Anpassen der Eigenschaft "CellSpacing" aktiviert automatisch den Zellenabstand.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
