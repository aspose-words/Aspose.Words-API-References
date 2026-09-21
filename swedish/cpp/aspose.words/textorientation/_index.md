---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextOrientation enum. Anger orientering av text på en sida, i en tabellcell eller i en textram i C++."
type: docs
weight: 124000
url: /sv/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Anger orienteringen av text på en sida, i en tabellcell eller i en textram.

```cpp
enum class TextOrientation
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Horisontell | 0 | Texten är ordnad horisontellt (lr-tb). |
| Nedåt | 1 | Texten roteras 90 grader åt höger för att visas från topp till botten (tb-rl). |
| Uppåt | 3 | Texten roteras 90 grader åt vänster för att visas från botten till toppen (bt-lr). |
| HorizontalRotatedFarEast | 4 | Texten är ordnad horisontellt, men Far East-tecken roteras 90 grader åt vänster (lr-tb-v). |
| VerticalFarEast | 5 | Far East-tecken visas vertikalt, annan text roteras 90 grader åt höger för att visas från topp till botten (tb-rl-v). |
| VerticalRotatedFarEast | 7 | Far East-tecken visas vertikalt, annan text roteras 90 grader åt höger för att visas från topp till botten vertikalt, sedan från vänster till höger horisontellt (tb-lr-v). |


## Exempel



Visar hur man bygger en formaterad 2x2-tabell.
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

// När tabellen byggs kommer dokumentbyggaren att tillämpa sina aktuella RowFormat/CellFormat-egenskapsvärden.
// på den aktuella rad/cell som dess markör befinner sig i och på alla nya rader/celler när den skapar dem.
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

// Tidigare tillagda rader och celler påverkas inte retroaktivt av förändringar i byggarens formatering.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
