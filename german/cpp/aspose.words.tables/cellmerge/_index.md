---
title: "Aspose::Words::Tables::CellMerge enum"
linktitle: "CellMerge"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellMerge enum. Gibt an, wie eine Zelle in einer Tabelle mit anderen Zellen in C++ zusammengeführt wird."
type: docs
weight: 11000
url: /de/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Gibt an, wie eine Zelle in einer Tabelle mit anderen Zellen zusammengeführt wird.

```cpp
enum class CellMerge
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Die Zelle ist nicht zusammengeführt. |
| Erste | 1 | Die Zelle ist die erste Zelle in einem Bereich zusammengeführter Zellen. |
| Vorherige | 2 | Die Zelle ist horizontal oder vertikal mit der vorherigen Zelle zusammengeführt. |


## Beispiele



Zeigt, wie Tabellenzellen vertikal zusammengeführt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Zelle in die erste Spalte der ersten Zeile ein.
// Diese Zelle wird die erste in einem Bereich vertikal zusammengeführter Zellen sein.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Fügen Sie eine Zelle in die zweite Spalte der ersten Zeile ein und beenden Sie anschließend die Zeile.
// Konfigurieren Sie außerdem den Builder, um das vertikale Zusammenführen in erstellten Zellen zu deaktivieren.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Fügen Sie eine Zelle in die erste Spalte der zweiten Zeile ein.
// Anstatt Textinhalte hinzuzufügen, werden wir diese Zelle mit der ersten Zelle zusammenführen, die wir direkt darüber eingefügt haben.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Fügen Sie eine weitere unabhängige Zelle in die zweite Spalte der zweiten Zeile ein.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


Zeigt, wie Tabellenzellen horizontal zusammengeführt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Zelle in die erste Spalte der ersten Zeile ein.
// Diese Zelle wird die erste in einem Bereich horizontal zusammengeführter Zellen sein.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Fügen Sie eine Zelle in die zweite Spalte der ersten Zeile ein. Anstatt Textinhalte hinzuzufügen,
// werden wir diese Zelle mit der ersten Zelle zusammenführen, die wir direkt links eingefügt haben.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Fügen Sie der zweiten Zeile zwei weitere nicht zusammengeführte Zellen hinzu.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
