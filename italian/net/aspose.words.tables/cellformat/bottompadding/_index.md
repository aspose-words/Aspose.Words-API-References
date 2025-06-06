---
title: CellFormat.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words per .NET
description: Scopri la proprietà CellFormat BottomPadding per personalizzare la spaziatura nelle celle. Migliora i tuoi layout con regolazioni precise dei punti per una presentazione migliore.
type: docs
weight: 20
url: /it/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

Restituisce o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto della cella.

```csharp
public double BottomPadding { get; set; }
```

## Esempi

Mostra come formattare le celle con un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Inserire una seconda cella, quindi configurare le opzioni di riempimento del testo della cella.
// Il builder applicherà queste impostazioni alla cella corrente e a tutte le nuove celle create in seguito.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// La prima cella non è stata interessata dalla riconfigurazione del padding e conserva ancora i valori predefiniti.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// La prima cella continuerà a crescere nel documento di output per adattarsi alle dimensioni della cella adiacente.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Guarda anche

* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
