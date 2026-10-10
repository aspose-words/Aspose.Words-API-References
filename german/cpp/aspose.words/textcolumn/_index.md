---
title: "Aspose::Words::TextColumn Klasse"
linktitle: "TextColumn"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumn Klasse. Stellt eine einzelne Textspalte dar. TextColumn ist ein Mitglied der TextColumnCollection-Sammlung. Die TextColumn-Sammlung enthält alle Spalten in einem Abschnitt eines Dokuments. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 70000
url: /de/cpp/aspose.words/textcolumn/
---
## TextColumn class


Stellt eine einzelne Textspalte dar. [TextColumn](./) ist ein Mitglied der Sammlung [TextColumnCollection](../textcolumncollection/). Die Sammlung [TextColumn](./) enthält alle Spalten in einem Abschnitt eines Dokuments. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Liest oder legt den Abstand zwischen dieser Spalte und der nächsten Spalte in Punkten fest. Für die letzte Spalte nicht erforderlich. |
| [get_Width](./get_width/)() | Liest oder legt die Breite der Textspalte in Punkten fest. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Setter für [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Setter für [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Hinweise


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

Wenn ein neues [TextColumn](./) erstellt wird, sind seine Breite und sein Abstand auf Null gesetzt.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
