---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::TableStyleOptions enum. Specifica come lo stile della tabella viene applicato a una tabella in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Specifica come lo stile della tabella viene applicato a una tabella.

```cpp
enum class TableStyleOptions
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Nessuna formattazione dello stile della tabella viene applicata. |
| FirstRow | 32 | Applica la formattazione condizionale alla prima riga. |
| LastRow | 64 | Applica la formattazione condizionale all'ultima riga. |
| FirstColumn | 128 | Applica la formattazione condizionale alla prima colonna 1. |
| LastColumn | 256 | Applica la formattazione condizionale all'ultima colonna. |
| RowBands | 512 | Applica la formattazione condizionale a bande di righe. |
| ColumnBands | 1024 | Applica la formattazione condizionale a bande di colonne. |
| Default2003 | n/a | [Row](../row/) e le bande di colonne vengono applicate. Questo è il valore predefinito di Microsoft Word per i vecchi formati come DOC, WML e RTF. |
| Default | n/a | Questi sono i valori predefiniti di Microsoft Word. |


## Esempi



Mostra come creare una nuova tabella applicando uno stile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Dobbiamo inserire almeno una riga prima di impostare qualsiasi formattazione della tabella.
builder->InsertCell();

// Imposta lo stile della tabella da utilizzare in base all'identificatore dello stile.
// Nota che non tutti gli stili di tabella sono disponibili quando si salva nel formato .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Applica parzialmente lo stile alle caratteristiche della tabella in base a predicati, quindi costruisci la tabella.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
