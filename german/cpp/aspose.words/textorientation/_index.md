---
title: "Aspose::Words::TextOrientation Enum"
linktitle: "TextOrientation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextOrientation Enum. Gibt die Ausrichtung von Text auf einer Seite, in einer Tabellenzelle oder in einem Textrahmen in C++ an."
type: docs
weight: 124000
url: /de/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Gibt die Ausrichtung von Text auf einer Seite, in einer Tabellenzelle oder einem Textrahmen an.

```cpp
enum class TextOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | 0 | Text wird horizontal angeordnet (lr-tb). |
| Abwärts | 1 | Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl). |
| Aufwärts | 3 | Der Text ist um 90 Grad nach links gedreht, um von unten nach oben zu erscheinen (bt-lr). |
| HorizontalRotatedFarEast | 4 | Der Text ist horizontal angeordnet, aber die Zeichen aus Fernost sind um 90 Grad nach links gedreht (lr-tb-v). |
| VerticalFarEast | 5 | Zeichen aus Fernost erscheinen vertikal, anderer Text ist um 90 Grad nach rechts gedreht, um von oben nach unten zu erscheinen (tb-rl-v). |
| VerticalRotatedFarEast | 7 | Zeichen aus Fernost erscheinen vertikal, anderer Text ist um 90 Grad nach rechts gedreht, um vertikal von oben nach unten zu erscheinen, dann horizontal von links nach rechts (tb-lr-v). |


## Beispiele



Zeigt, wie man eine formatierte 2x2‑Tabelle erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Während der Erstellung der Tabelle wendet der Document Builder seine aktuellen RowFormat/CellFormat‑Eigenschaftswerte an
// auf die aktuelle Zeile/Zelle, in der sich der Cursor befindet, und auf alle neuen Zeilen/Zellen, die er erstellt.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Zuvor hinzugefügte Zeilen und Zellen werden nicht rückwirkend von Änderungen der Formatierung des Builders beeinflusst.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
