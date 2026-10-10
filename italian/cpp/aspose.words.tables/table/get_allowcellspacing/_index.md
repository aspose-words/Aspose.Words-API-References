---
title: "Metodo Aspose::Words::Tables::Table::get_AllowCellSpacing"
linktitle: "get_AllowCellSpacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Table::get_AllowCellSpacing. Ottiene o imposta l'opzione \\\"Consenti spaziatura tra le celle\\\" in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Ottiene o imposta l'opzione "Allow spacing between cells".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Esempi



Mostra come abilitare la spaziatura tra le singole celle in una tabella.
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

// Imposta la proprietà \"AllowCellSpacing\" su \"true\" per abilitare la spaziatura tra le celle
// con una magnitudine pari al valore della proprietà \"CellSpacing\", in punti.
// Imposta la proprietà \"AllowCellSpacing\" su \"false\" per disabilitare la spaziatura tra le celle
// e ignora il valore della proprietà \"CellSpacing\".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Regolare la proprietà \"CellSpacing\" abiliterà automaticamente la spaziatura tra le celle.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
