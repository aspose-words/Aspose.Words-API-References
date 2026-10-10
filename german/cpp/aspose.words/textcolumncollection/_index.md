---
title: "Aspose::Words::TextColumnCollection Klasse"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumnCollection Klasse. Eine Sammlung von TextColumn‑Objekten, die alle Textspalten in einem Abschnitt eines Dokuments darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 71000
url: /de/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


Eine Sammlung von [TextColumn](../textcolumn/)-Objekten, die alle Textspalten in einem Abschnitt eines Dokuments darstellen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Ermittelt die Anzahl der Spalten im Abschnitt eines Dokuments. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | Wahr, wenn Textspalten gleiche Breite und gleichmäßigen Abstand haben. |
| [get_LineBetween](./get_linebetween/)() | Wenn **true**, wird eine vertikale Linie zwischen den Spalten hinzugefügt. |
| [get_Spacing](./get_spacing/)() | Wenn Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten ermittelt oder festgelegt. |
| [get_Width](./get_width/)() | Wenn Spalten gleichmäßig verteilt sind, wird die Breite der Spalten ermittelt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt eine Textspalte am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Setter für [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Setter für [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Setter für [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Ordnet den Text in die angegebene Anzahl von Textspalten ein. |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie [SetCount()](./setcount/), um die Anzahl der Textspalten festzulegen.

Um alle Spalten gleich breit und gleichmäßig verteilt zu machen, setzen Sie [EvenlySpaced](./get_evenlyspaced/) auf **true** und geben Sie den Abstand zwischen den Spalten in [Spacing](./get_spacing/) an. MS Word berechnet die Spaltenbreiten automatisch.

Wenn Sie [EvenlySpaced](./get_evenlyspaced/) auf **false** gesetzt haben, müssen Sie Breite und Abstand für jede Spalte einzeln angeben. Verwenden Sie den Indexer, um auf einzelne [TextColumn](../textcolumn/) Objekte zuzugreifen.

Wenn Sie benutzerdefinierte Spaltenbreiten verwenden, stellen Sie sicher, dass die Summe aller Spaltenbreiten und Abstände zwischen ihnen der Seitenbreite minus den linken und rechten Seitenrändern entspricht.

## Beispiele



Zeigt, wie man mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
