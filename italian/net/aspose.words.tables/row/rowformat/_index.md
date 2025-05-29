---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà Row RowFormat per accedere facilmente alle opzioni di formattazione delle righe personalizzabili, migliorando così la presentazione dei tuoi dati senza sforzo.
type: docs
weight: 110
url: /it/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Fornisce l'accesso alle proprietà di formattazione della riga.

```csharp
public RowFormat RowFormat { get; }
```

## Esempi

Mostra come modificare la formattazione di una riga di una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Utilizzare la proprietà "RowFormat" della prima riga per impostare la formattazione che modifica l'aspetto dell'intera riga.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
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

// Utilizzare la proprietà "RowFormat" della prima riga per modificare la formattazione
// del contenuto di tutte le celle in questa riga.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Utilizzare la proprietà "CellFormat" della prima cella nell'ultima riga per modificare la formattazione del contenuto di quella cella.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Guarda anche

* class [RowFormat](../../rowformat/)
* class [Row](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
