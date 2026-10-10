---
title: "Aspose::Words::Tables::Table::get_PreferredWidth metodo"
linktitle: "get_PreferredWidth"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_PreferredWidth metodo. Ottiene o imposta la larghezza preferita della tabella in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Ottiene o imposta la larghezza preferita della tabella.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Note


Il valore predefinito è [Auto](../../preferredwidth/auto/).

## Esempi



Mostra come impostare una tabella per adattarsi automaticamente al 50% della larghezza della pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## Vedi anche

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
