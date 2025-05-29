---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table StyleIdentifier per gestire facilmente stili di tabella indipendenti dalle impostazioni locali, migliorando senza sforzo la presentazione dei tuoi dati.
type: docs
weight: 280
url: /it/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Ottiene o imposta l'identificatore di stile indipendente dalle impostazioni locali dello stile di tabella applicato a questa tabella.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

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

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
