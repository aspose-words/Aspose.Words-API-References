---
title: DocumentBuilder.InsertCell
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce una cella di tabella nel documento.
type: docs
weight: 270
url: /it/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Inserisce una cella di tabella nel documento.

```csharp
public Cell InsertCell()
```

### Valore di ritorno

Il nodo della cella appena inserito.

### Osservazioni

Per avviare un tavolo, basta chiamare`InsertCell` . Successivamente, qualsiasi contenuto aggiunto utilizzando altri metodi del[`DocumentBuilder`](../) la classe verrà aggiunta alla cella corrente.

Per iniziare una nuova cella nella stessa riga, chiama`InsertCell` Ancora.

Per terminare una chiamata alla riga di una tabella[`EndRow`](../endrow/).

Usa il[`CellFormat`](../cellformat/)proprietà per specificare la formattazione della cella.

### Esempi

Mostra come utilizzare un generatore di documenti per creare una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inizia la tabella, quindi compila la prima riga con due celle.
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
// li applicherà a ogni riga e cella che aggiungiamo con esso.
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

// La modifica della formattazione la applicherà alla cella corrente,
// e tutte le nuove celle che creeremo successivamente con il builder.
// Ciò non influenzerà le celle che abbiamo aggiunto in precedenza.
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
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


