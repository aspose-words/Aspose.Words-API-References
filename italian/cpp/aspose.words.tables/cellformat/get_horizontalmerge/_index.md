---
title: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge metodo"
linktitle: "get_HorizontalMerge"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge metodo. Specifica come la cella viene unita orizzontalmente con altre celle nella riga in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Specifica come la cella è unita orizzontalmente con altre celle nella riga.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Esempi



Mostra come unire le celle della tabella orizzontalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una cella nella prima colonna della prima riga.
// Questa cella sarà la prima in un intervallo di celle unite orizzontalmente.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Inserisci una cella nella seconda colonna della prima riga. Invece di aggiungere contenuti di testo,
// uniremo questa cella con la prima cella che abbiamo aggiunto direttamente a sinistra.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Inserisci altre due celle non unite nella seconda riga.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## Vedi anche

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
