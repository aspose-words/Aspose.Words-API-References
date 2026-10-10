---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::TextWrapping enum. Anger hur texten omsluts runt tabellen i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Anger hur text flödar runt tabellen.

```cpp
enum class TextWrapping
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Text och tabell visas i den ordning de förekommer i dokumentet. |
| Runt | 1 | Texten omsluts runt tabellen och upptar tillgängligt sidutrymme. |
| Standard | n/a | Standardvärde. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
