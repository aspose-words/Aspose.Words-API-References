---
title: "Aspose::Words::Tables::Cell::get_FirstParagraph Methode"
linktitle: "get_FirstParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Cell::get_FirstParagraph Methode. Gibt den ersten Absatz unter den unmittelbaren Kindknoten in C++ zurück."
type: docs
weight: 6000
url: /de/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Ermittelt den ersten Absatz unter den unmittelbaren Kindknoten.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Beispiele



Zeigt, wie man mit einem DocumentBuilder eine verschachtelte Tabelle erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle die äußere Tabelle.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Gehe zur ersten Zelle der äußeren Tabelle und erstelle dann eine weitere Tabelle innerhalb der Zelle.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## Siehe auch

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
