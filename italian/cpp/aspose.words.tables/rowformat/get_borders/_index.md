---
title: "Aspose::Words::Tables::RowFormat::get_Borders method"
linktitle: "get_Borders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::RowFormat::get_Borders method. Ottiene la collezione dei bordi di cella predefiniti per la riga in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.tables/rowformat/get_borders/
---
## RowFormat::get_Borders method


Ottiene la raccolta dei bordi predefiniti delle celle per la riga.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Tables::RowFormat::get_Borders()
```


## Esempi



Mostra come costruire una tabella con bordi personalizzati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Impostazione delle opzioni di formattazione della tabella per un DocumentBuilder
// le applicherà a ogni riga e cella che aggiungiamo con esso.
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

// Modificando la formattazione la applicherà alla cella corrente,
// e a tutte le nuove celle che creiamo con il builder in seguito.
// Questo non influenzerà le celle che abbiamo aggiunto in precedenza.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Aumenta l'altezza della riga per adattare il testo verticale.
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

## Vedi anche

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
