---
title: RowFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words per .NET
description: Scopri la proprietà RowFormat Height per regolare facilmente l'altezza delle righe della tabella in punti, migliorando il layout e la leggibilità del tuo documento.
type: docs
weight: 40
url: /it/net/aspose.words.tables/rowformat/height/
---
## RowFormat.Height property

Ottiene o imposta l'altezza della riga della tabella in punti.

```csharp
public double Height { get; set; }
```

## Esempi

Mostra come formattare le righe con un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Avvia una seconda riga e quindi configurane l'altezza. Il builder applicherà queste impostazioni a
// la sua riga corrente, nonché tutte le nuove righe che crea in seguito.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// La prima riga non è stata interessata dalla riconfigurazione del padding e mantiene ancora i valori predefiniti.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

Mostra come creare una tabella formattata utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Imposta alcune opzioni di formattazione per l'aspetto del testo e della tabella.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// La configurazione delle opzioni di formattazione in un generatore di documenti le applicherà
// alla cella/riga corrente in cui si trova il cursore,
// nonché tutte le nuove celle e righe create utilizzando quel generatore.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Riconfiguriamo gli oggetti di formattazione del builder per le nuove righe e celle che stiamo per creare.
// Il builder non applicherà queste modifiche alla prima riga già creata, in modo che questa risalti come riga di intestazione.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Guarda anche

* class [RowFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
