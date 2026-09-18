---
title: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge Methode"
linktitle: "get_HorizontalMerge"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge Methode. Gibt an, wie die Zelle horizontal mit anderen Zellen in der Zeile in C++ zusammengeführt wird."
type: docs
weight: 6000
url: /de/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Gibt an, wie die Zelle horizontal mit anderen Zellen in der Zeile zusammengeführt wird.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Beispiele



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

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
