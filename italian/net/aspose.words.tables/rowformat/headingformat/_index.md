---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà RowFormat HeadingFormat e assicurati che le intestazioni delle tabelle vengano ripetute in ogni pagina per maggiore chiarezza e leggibilità nei documenti multipagina.
type: docs
weight: 30
url: /it/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Vero se la riga viene ripetuta come intestazione di tabella su ogni pagina quando la tabella si estende su più di una pagina.

```csharp
public bool HeadingFormat { get; set; }
```

## Esempi

Mostra come creare una tabella con righe che si ripetono in ogni pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Tutte le righe inserite mentre il flag "HeadingFormat" è impostato su "true"
// verrà visualizzato in cima alla tabella in ogni pagina in cui si estende.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Aggiungere righe sufficienti affinché la tabella si estenda su due pagine.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### Guarda anche

* class [RowFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
