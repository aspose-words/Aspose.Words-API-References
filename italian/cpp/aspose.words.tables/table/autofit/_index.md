---
title: "Aspose::Words::Tables::Table::AutoFit metodo"
linktitle: "AutoFit"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::AutoFit metodo. Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato.

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| comportamento | Aspose::Words::Tables::AutoFitBehavior | Specifica come adattare automaticamente la tabella. |
## Note


Questo metodo imita i comandi disponibili nel menu Auto Fit per una tabella in Microsoft Word. I comandi disponibili sono "Auto Fit to Contents", "Auto Fit to Window" e "Fixed Column Width". In Microsoft Word questi comandi impostano le proprietà rilevanti della tabella e quindi aggiornano il layout della tabella e Aspose.Words fa lo stesso per te.

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

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
