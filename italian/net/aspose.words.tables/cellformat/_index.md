---
title: CellFormat
second_title: Aspose.Words per .NET API Reference
description: Rappresenta tutta la formattazione per una cella di tabella.
type: docs
weight: 5960
url: /it/net/aspose.words.tables/cellformat/
---
## CellFormat class

Rappresenta tutta la formattazione per una cella di tabella.

```csharp
public class CellFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders) { get; } | Ottiene la raccolta dei bordi della cella. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding) { get; set; } | Restituisce o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto della cella. |
| [FitText](../../aspose.words.tables/cellformat/fittext) { get; set; } | Se true, adatta il testo alla cella, comprimendo ogni paragrafo alla larghezza della cella. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge) { get; set; } | Specifica come la cella viene unita orizzontalmente con altre celle nella riga. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding) { get; set; } | Restituisce o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto della cella. |
| [Orientation](../../aspose.words.tables/cellformat/orientation) { get; set; } | Restituisce o imposta l'orientamento del testo in una cella di tabella. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth) { get; set; } | Restituisce o imposta la larghezza preferita della cella. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding) { get; set; } | Restituisce o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto della cella. |
| [Shading](../../aspose.words.tables/cellformat/shading) { get; } | Restituisce un oggetto Shading che fa riferimento alla formattazione dell'ombreggiatura per la cella. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding) { get; set; } | Restituisce o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto della cella. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment) { get; set; } | Restituisce o imposta l'allineamento verticale del testo nella cella. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge) { get; set; } | Specifica come la cella viene unita alle altre celle verticalmente. |
| [Width](../../aspose.words.tables/cellformat/width) { get; set; } | Ottiene la larghezza della cella in punti. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext) { get; set; } | Se vero, manda a capo il testo per la cella. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting)() | Ripristina la formattazione della cella predefinita. Non cambia la larghezza della cella. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings)(double, double, double, double) | Imposta la quantità di spazio (in punti) da aggiungere a sinistra/in alto/a destra/in basso del contenuto della cella. |

### Esempi

Mostra come modificare la formattazione di una cella di tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Usa la proprietà "CellFormat" di una cella per impostare la formattazione che modifica l'aspetto di quella cella.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Mostra come modificare il formato di righe e celle in una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Usa la proprietà "RowFormat" della prima riga per modificare la formattazione
// del contenuto di tutte le celle in questa riga.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Usa la proprietà "CellFormat" della prima cella nell'ultima riga per modificare la formattazione del contenuto di quella cella.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
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
// e tutte le nuove celle che creiamo con il builder in seguito.
// Ciò non influirà sulle celle che abbiamo aggiunto in precedenza.
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

* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
