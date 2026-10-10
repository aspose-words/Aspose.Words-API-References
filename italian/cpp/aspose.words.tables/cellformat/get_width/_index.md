---
title: "Aspose::Words::Tables::CellFormat::get_Width metodo"
linktitle: "get_Width"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellFormat::get_Width metodo. Ottiene la larghezza della cella in punti in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.tables/cellformat/get_width/
---
## CellFormat::get_Width method


Ottiene la larghezza della cella in punti.

```cpp
double Aspose::Words::Tables::CellFormat::get_Width()
```

## Note


La larghezza è calcolata da Aspose.Words durante il caricamento e il salvataggio del documento. Attualmente, non tutte le combinazioni di proprietà di tabella, cella e documento sono supportate. Il valore restituito potrebbe non essere accurato per alcuni documenti. Potrebbe non corrispondere esattamente alla larghezza della cella calcolata da MS Word quando il documento viene aperto in MS Word.

Impostare questa proprietà non è consigliato. Non vi è alcuna garanzia che la cella abbia effettivamente la larghezza impostata. La larghezza può essere regolata per adattarsi al contenuto della cella in un layout di tabella a dimensionamento automatico. Le celle in altre righe possono avere impostazioni di larghezza conflittuali. La tabella può essere ridimensionata per adattarsi al contenitore o per soddisfare le impostazioni di larghezza della tabella. Considera l'uso di [PreferredWidth](../get_preferredwidth/) per impostare la larghezza della cella. L'impostazione di questa proprietà imposta implicitamente [PreferredWidth](../get_preferredwidth/) dalla versione 15.8.

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


Mostra come formattare le celle con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Inserisci una seconda cella, quindi configura le opzioni di padding del testo della cella.
// Il builder applicherà queste impostazioni alla sua cella corrente, e qualsiasi nuova cella creata successivamente.
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

// La prima cella non è stata influenzata dalla riconfigurazione del padding e mantiene ancora i valori predefiniti.
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

// La prima cella continuerà a espandersi nel documento di output per corrispondere alle dimensioni della cella adiacente.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## Vedi anche

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
