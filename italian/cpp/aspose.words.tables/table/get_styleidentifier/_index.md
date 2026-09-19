---
title: "Metodo Aspose::Words::Tables::Table::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Table::get_StyleIdentifier. Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile di tabella applicato a questa tabella in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words.tables/table/get_styleidentifier/
---
## Table::get_StyleIdentifier method


Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile della tabella applicato a questa tabella.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Tables::Table::get_StyleIdentifier()
```


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

* Enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
