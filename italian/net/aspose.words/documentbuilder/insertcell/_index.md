---
title: DocumentBuilder.InsertCell
linktitle: InsertCell
articleTitle: InsertCell
second_title: Aspose.Words per .NET
description: Migliora senza sforzo i tuoi documenti con il metodo InsertCell di DocumentBuilder: aggiungi rapidamente celle di tabella personalizzabili per una migliore organizzazione e chiarezza.
type: docs
weight: 270
url: /it/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Inserisce una cella della tabella nel documento.

```csharp
public Cell InsertCell()
```

### Valore di ritorno

Il nodo cellulare appena inserito.

## Osservazioni

Per iniziare una tabella, basta chiamare`InsertCell` Dopo questo, qualsiasi contenuto aggiunto utilizzando altri metodi del[`DocumentBuilder`](../) la classe verrà aggiunta alla cella corrente.

Per iniziare una nuova cella nella stessa riga, chiamare`InsertCell` Ancora.

Per terminare una chiamata di riga di tabella[`EndRow`](../endrow/).

Utilizzare il[`CellFormat`](../cellformat/) proprietà per specificare la formattazione della cella.

## Esempi

Mostra come utilizzare un generatore di documenti per creare una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Avvia la tabella, quindi popola la prima riga con due celle.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Chiama il metodo "EndRow" del builder per iniziare una nuova riga.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
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

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
