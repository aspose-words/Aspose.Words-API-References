---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table StyleOptions per personalizzare l'aspetto della tua tabella con flag di bit flessibili. Migliora lo stile della tua tabella senza sforzo!
type: docs
weight: 300
url: /it/net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

Ottiene o imposta i flag di bit che specificano come uno stile di tabella viene applicato a questa tabella.

```csharp
public TableStyleOptions StyleOptions { get; set; }
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

* enum [TableStyleOptions](../../tablestyleoptions/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
