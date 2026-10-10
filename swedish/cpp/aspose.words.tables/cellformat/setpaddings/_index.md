---
title: "Aspose::Words::Tables::CellFormat::SetPaddings metod"
linktitle: "SetPaddings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellFormat::SetPaddings method. Anger mängden utrymme (i punkter) som ska läggas till vänster/upp/höger/nederkant av cellens innehåll i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Anger mängden utrymme (i punkter) som ska läggas till vänster/upp/höger/nederst av cellens innehåll.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Exempel



Visar hur man fyller cellens innehåll med blanksteg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ange ett utfyllnadsavstånd (i punkter) mellan kanten och textinnehållet
// för varje tabellcell som vi skapar med dokumentbyggaren.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Skapa en tabell med en cell vars innehåll kommer att ha blankstegsutfyllnad.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## Se även

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
