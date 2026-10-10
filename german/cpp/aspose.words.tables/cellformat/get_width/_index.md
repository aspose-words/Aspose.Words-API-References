---
title: "Aspose::Words::Tables::CellFormat::get_Width-Methode"
linktitle: "get_Width"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::get_Width-Methode. Gibt die Breite der Zelle in Punkten in C++ zurück."
type: docs
weight: 15000
url: /de/cpp/aspose.words.tables/cellformat/get_width/
---
## CellFormat::get_Width method


Ermittelt die Breite der Zelle in Punkten.

```cpp
double Aspose::Words::Tables::CellFormat::get_Width()
```

## Hinweise


Die Breite wird von Aspose.Words beim Laden und Speichern des Dokuments berechnet. Derzeit wird nicht jede Kombination von Tabellen-, Zellen- und Dokumenteigenschaften unterstützt. Der zurückgegebene Wert ist für einige Dokumente möglicherweise nicht genau. Er stimmt möglicherweise nicht exakt mit der von MS Word berechneten Zellenbreite überein, wenn das Dokument in MS Word geöffnet wird.

Das Festlegen dieser Eigenschaft wird nicht empfohlen. Es gibt keine Garantie, dass die Zelle tatsächlich die eingestellte Breite hat. Die Breite kann angepasst werden, um den Zelleninhalt in einem automatischen Tabellenlayout aufzunehmen. Zellen in anderen Zeilen können widersprüchliche Breiteneinstellungen haben. Die Tabelle kann in der Größe angepasst werden, um in den Container zu passen oder die Tabelleneinstellungen zu erfüllen. Erwägen Sie die Verwendung von [PreferredWidth](../get_preferredwidth/) zum Festlegen der Zellenbreite. Das Festlegen dieser Eigenschaft setzt [PreferredWidth](../get_preferredwidth/) implizit seit Version 15.8.

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


Zeigt, wie man Zellen mit einem DocumentBuilder formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Fügen Sie eine zweite Zelle ein und konfigurieren Sie dann die Optionen für den Zelltext‑Abstand.
// Der Builder wendet diese Einstellungen auf seine aktuelle Zelle an, und alle danach erstellten neuen Zellen übernehmen sie.
builder->InsertCell();

System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = builder->get_CellFormat();
cellFormat->set_Width(250);
cellFormat->set_LeftPadding(30);
cellFormat->set_RightPadding(30);
cellFormat->set_TopPadding(30);
cellFormat->set_BottomPadding(30);

builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->EndTable();

// Die erste Zelle war von der Neukonfiguration des Abstands unbeeinflusst und behält weiterhin die Standardwerte.
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_BottomPadding());

ASPOSE_ASSERT_EQ(250.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_BottomPadding());

// Die erste Zelle wird im Ausgabedokument weiterhin wachsen, um die Größe der benachbarten Zelle anzupassen.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## Siehe auch

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
