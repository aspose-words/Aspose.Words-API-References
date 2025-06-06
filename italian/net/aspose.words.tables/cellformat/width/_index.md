---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words per .NET
description: Scopri la proprietà CellFormat Width per misurare facilmente la larghezza delle celle in punti, migliorando così il layout e la leggibilità del tuo foglio di calcolo.
type: docs
weight: 140
url: /it/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Ottiene la larghezza della cella in punti.

```csharp
public double Width { get; set; }
```

## Osservazioni

La larghezza viene calcolata da Aspose.Words durante il caricamento e il salvataggio del documento. Attualmente, non sono supportate tutte le combinazioni di proprietà di tabelle, celle e documenti. Il valore restituito potrebbe non essere accurato per alcuni documenti. Potrebbe non corrispondere esattamente alla larghezza della cella calcolata da MS Word quando il documento viene aperto in MS Word.

L'impostazione di questa proprietà non è consigliata. Non vi è alcuna garanzia che la cella avrà effettivamente la larghezza impostata. La larghezza può essere regolata per accogliere il contenuto della cella in un layout di tabella con adattamento automatico. Le celle in altre righe potrebbero avere impostazioni di larghezza in conflitto. La tabella può essere ridimensionata per adattarsi al contenitore o per soddisfare le impostazioni di larghezza della tabella. Si consiglia di utilizzare[`PreferredWidth`](../preferredwidth/)per impostare la larghezza della cella. L'impostazione di questa proprietà imposta[`PreferredWidth`](../preferredwidth/) implicitamente dalla versione 15.8.

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

Mostra come creare una tabella con bordi personalizzati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Impostazione delle opzioni di formattazione della tabella per un generatore di documenti
// li applicheremo a ogni riga e cella che aggiungeremo.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// La modifica della formattazione verrà applicata alla cella corrente,
// e tutte le nuove celle che creeremo in seguito con il builder.
// Ciò non influirà sulle celle aggiunte in precedenza.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Aumenta l'altezza della riga per adattarla al testo verticale.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Guarda anche

* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
