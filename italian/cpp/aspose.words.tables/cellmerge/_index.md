---
title: "Aspose::Words::Tables::CellMerge enum"
linktitle: "CellMerge"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellMerge enum. Specifica come una cella in una tabella viene unita ad altre celle in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Specifica come una cella in una tabella viene unita ad altre celle.

```cpp
enum class CellMerge
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | La cella non è unita. |
| Prima | 1 | La cella è la prima cella in un intervallo di celle unite. |
| Precedente | 2 | La cella è unita alla cella precedente orizzontalmente o verticalmente. |


## Esempi



Mostra come unire le celle della tabella verticalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una cella nella prima colonna della prima riga.
// Questa cella sarà la prima in un intervallo di celle unite verticalmente.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Inserisci una cella nella seconda colonna della prima riga, poi termina la riga.
// Inoltre, configura il builder per disabilitare l'unione verticale nelle celle create.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Inserisci una cella nella prima colonna della seconda riga.
// Invece di aggiungere contenuti di testo, uniremo questa cella con la prima cella che abbiamo aggiunto direttamente sopra.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Inserisci un'altra cella indipendente nella seconda colonna della seconda riga.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
