---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words per .NET
description: Table AutoFit metodo. Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato in C#.
type: docs
weight: 360
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

Questo metodo imita i comandi disponibili nel menu Adattamento automatico per una tabella in Microsoft Word. I comandi disponibili sono "Adatta automaticamente al contenuto", "Adatta automaticamente alla finestra" e "Larghezza colonna fissa". In Microsoft Word questi comandi impostano le proprietà rilevanti della tabella e quindi aggiornano il layout della tabella e Aspose.Words fa lo stesso per te.

## Esempi

Mostra come creare una nuova tabella durante l'applicazione di uno stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Dobbiamo inserire almeno una riga prima di impostare qualsiasi formattazione della tabella.
builder.InsertCell();

// Imposta lo stile della tabella utilizzato in base all'identificatore dello stile.
// Tieni presente che non tutti gli stili di tabella sono disponibili quando si salva nel formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Applica parzialmente lo stile alle funzionalità della tabella in base ai predicati, quindi crea la tabella.
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
