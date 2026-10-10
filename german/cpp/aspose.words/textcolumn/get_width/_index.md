---
title: "Aspose::Words::TextColumn::get_Width‑Methode"
linktitle: "get_Width"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumn::get_Width‑Methode. Gibt die Breite der Textspalte in Punkten zurück oder legt sie fest in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/textcolumn/get_width/
---
## TextColumn::get_Width method


Liest oder legt die Breite der Textspalte in Punkten fest.

```cpp
double Aspose::Words::TextColumn::get_Width()
```


## Beispiele



Zeigt, wie man ungleichmäßig platzierte Spalten erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Bestimmen Sie den verfügbaren Platz für die Anordnung von Spalten.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Setzen Sie die erste Spalte schmal.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Setzen Sie die zweite Spalte so, dass sie den restlichen verfügbaren Platz innerhalb der Seitenränder einnimmt.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Siehe auch

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
