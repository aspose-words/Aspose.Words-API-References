---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge Methode"
linktitle: "get_VerticalMerge"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge Methode. Gibt an, wie die Zelle vertikal mit anderen Zellen in C++ zusammengeführt wird."
type: docs
weight: 14000
url: /de/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Gibt an, wie die Zelle vertikal mit anderen Zellen zusammengeführt wird.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Hinweise


Zellen können nur vertikal zusammengeführt werden, wenn ihre linken und rechten Grenzen identisch sind.

Wenn Zellen vertikal zusammengeführt werden, werden die Anzeigebereiche der zusammengeführten Zellen konsolidiert. Der konsolidierte Bereich wird verwendet, um den Inhalt der ersten vertikal zusammengeführten Zelle anzuzeigen, und alle anderen vertikal zusammengeführten Zellen müssen leer sein.

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

## Siehe auch

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
