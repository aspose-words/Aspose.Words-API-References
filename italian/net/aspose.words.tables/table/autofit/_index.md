---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words per .NET
description: Scopri il metodo "Adattamento automatico tabelle" per ridimensionare facilmente tabelle e celle e ottenere un layout ottimale. Migliora la presentazione dei tuoi documenti con facilità!
type: docs
weight: 380
url: /it/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| behavior | AutoFitBehavior | Specifica come adattare automaticamente la tabella. |

## Osservazioni

Questo metodo imita i comandi disponibili nel menu "Adattamento automatico" per una tabella in Microsoft Word. I comandi disponibili sono "Adattamento automatico al contenuto", "Adattamento automatico alla finestra" e "Larghezza colonna fissa". In Microsoft Word, questi comandi impostano le proprietà della tabella e ne aggiornano il layout, mentre Aspose.Words fa lo stesso.

## Esempi

Mostra come creare una nuova tabella applicando uno stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Dobbiamo inserire almeno una riga prima di impostare qualsiasi formattazione della tabella.
builder.InsertCell();

// Imposta lo stile della tabella utilizzato in base all'identificatore di stile.
// Nota che non tutti gli stili di tabella sono disponibili quando si salva in formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Applica parzialmente lo stile alle caratteristiche della tabella in base ai predicati, quindi crea la tabella.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Guarda anche

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
