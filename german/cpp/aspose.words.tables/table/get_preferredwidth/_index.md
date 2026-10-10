---
title: "Aspose::Words::Tables::Table::get_PreferredWidth Methode"
linktitle: "get_PreferredWidth"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_PreferredWidth Methode. Ruft die bevorzugte Tabellenbreite ab oder legt sie fest in C++."
type: docs
weight: 29000
url: /de/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Liest oder legt die bevorzugte Breite der Tabelle fest.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Hinweise


Der Standardwert ist [Auto](../../preferredwidth/auto/).

## Beispiele



Zeigt, wie man eine Tabelle so einstellt, dass sie automatisch auf 50 % der Seitenbreite passt.
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

## Siehe auch

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
