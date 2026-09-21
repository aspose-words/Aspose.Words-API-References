---
title: "Aspose::Words::Tables::Table::get_PreferredWidth metod"
linktitle: "get_PreferredWidth"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_PreferredWidth metod. Hämtar eller anger den föredragna bredden för tabellen i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Hämtar eller anger tabellens föredragna bredd.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Anmärkningar


Standardvärdet är [Auto](../../preferredwidth/auto/).

## Exempel



Visar hur man ställer in en tabell så att den automatiskt anpassas till 50 % av sidans bredd.
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

## Se även

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
