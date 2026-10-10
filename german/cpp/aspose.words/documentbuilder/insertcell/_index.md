---
title: "Aspose::Words::DocumentBuilder::InsertCell Methode"
linktitle: "InsertCell"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertCell Methode. Fügt in C++ eine Tabellenzelle in das Dokument ein."
type: docs
weight: 29000
url: /de/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


Fügt eine Tabellenzelle in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

Der Zellenknoten, der gerade eingefügt wurde.
## Hinweise


Um eine Tabelle zu starten, rufen Sie einfach [InsertCell](./) auf. Danach wird jeder Inhalt, den Sie mit anderen Methoden der Klasse [DocumentBuilder](../) hinzufügen, zur aktuellen Zelle hinzugefügt.

Um eine neue Zelle in derselben Zeile zu starten, rufen Sie erneut [InsertCell](./) auf.

Um eine Tabellenzeile zu beenden, rufen Sie [EndRow](../endrow/) auf.

Verwenden Sie die Eigenschaft [CellFormat](../get_cellformat/), um die Zellformatierung festzulegen.

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


Zeigt, wie man einen DocumentBuilder verwendet, um eine Tabelle zu erstellen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Starten Sie die Tabelle und füllen Sie dann die erste Zeile mit zwei Zellen.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Rufen Sie die Methode "EndRow" des Builders auf, um eine neue Zeile zu beginnen.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Siehe auch

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
