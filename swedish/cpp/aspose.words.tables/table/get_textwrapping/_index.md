---
title: "Aspose::Words::Tables::Table::get_TextWrapping method"
linktitle: "get_TextWrapping"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_TextWrapping method. Hämtar eller anger TextWrapping för tabell i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


Hämtar eller anger [TextWrapping](./) för tabell.

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## Exempel



Visar hur man arbetar med tabelltextomslag.
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

// Ställ in egenskapen "TextWrapping" till "TextWrapping.Around" för att få tabellen att omsluta text runt den,
// och tryck ner den i stycket nedanför genom att ange positionen.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Se även

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
