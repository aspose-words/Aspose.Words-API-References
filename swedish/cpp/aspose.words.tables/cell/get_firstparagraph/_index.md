---
title: "Aspose::Words::Tables::Cell::get_FirstParagraph metod"
linktitle: "get_FirstParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Cell::get_FirstParagraph metod. Hämtar det första stycket bland de omedelbara barnen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Hämtar det första stycket bland de omedelbara barnen.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Exempel



Visar hur man skapar en nästlad tabell med en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bygg den yttre tabellen.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Flytta till den första cellen i den yttre tabellen, bygg sedan en annan tabell i cellen.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## Se även

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
