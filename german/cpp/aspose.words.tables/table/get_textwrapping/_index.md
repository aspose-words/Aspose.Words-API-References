---
title: "Aspose::Words::Tables::Table::get_TextWrapping-Methode"
linktitle: "get_TextWrapping"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_TextWrapping-Methode. Liest oder setzt TextWrapping für die Tabelle in C++."
type: docs
weight: 38000
url: /de/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


Liest oder setzt [TextWrapping](./) für die Tabelle.

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## Beispiele



Zeigt, wie man mit dem Textfluss um Tabellen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Setzen Sie die Eigenschaft "TextWrapping" auf "TextWrapping.Around", um die Tabelle dazu zu bringen, Text um sie herum zu fließen,
// und schieben Sie sie nach unten in den darunterliegenden Absatz, indem Sie die Position festlegen.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Siehe auch

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
