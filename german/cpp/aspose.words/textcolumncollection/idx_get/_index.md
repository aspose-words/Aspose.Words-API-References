---
title: "Aspose::Words::TextColumnCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumnCollection::idx_get Methode. Gibt eine Textspalte am angegebenen Index in C++ zurück."
type: docs
weight: 8000
url: /de/cpp/aspose.words/textcolumncollection/idx_get/
---
## TextColumnCollection::idx_get method


Gibt eine Textspalte am angegebenen Index zurück.

```cpp
System::SharedPtr<Aspose::Words::TextColumn> Aspose::Words::TextColumnCollection::idx_get(int32_t index)
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

* Class [TextColumn](../../textcolumn/)
* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
