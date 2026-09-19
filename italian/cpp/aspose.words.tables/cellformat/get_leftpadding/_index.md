---
title: "Aspose::Words::Tables::CellFormat::get_LeftPadding metodo"
linktitle: "get_LeftPadding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellFormat::get_LeftPadding metodo. Restituisce o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto della cella in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.tables/cellformat/get_leftpadding/
---
## CellFormat::get_LeftPadding method


Restituisce o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto della cella.

```cpp
double Aspose::Words::Tables::CellFormat::get_LeftPadding()
```


## Esempi



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
