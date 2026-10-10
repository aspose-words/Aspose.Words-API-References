---
title: "Aspose::Words::Shading::ClearFormatting Methode"
linktitle: "ClearFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Shading::ClearFormatting Methode. Entfernt die Schattierung vom Objekt in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/shading/clearformatting/
---
## Shading::ClearFormatting method


Entfernt die Schattierung aus dem Objekt.

```cpp
void Aspose::Words::Shading::ClearFormatting()
```


## Beispiele



Zeigt, wie man eine Tabelle mit benutzerdefinierten Rahmen erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen DocumentBuilder
// wird sie auf jede Zeile und Zelle anwenden, die wir damit hinzufügen.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Das Ändern der Formatierung wird sie auf die aktuelle Zelle anwenden,
// und auf alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies wird die bereits zuvor hinzugefügten Zellen nicht beeinflussen.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Erhöhen Sie die Zeilenhöhe, um den vertikalen Text anzupassen.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```

## Siehe auch

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
