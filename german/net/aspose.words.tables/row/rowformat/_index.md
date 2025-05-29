---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die RowFormat-Eigenschaft für den einfachen Zugriff auf anpassbare Zeilenformatierungsoptionen und verbessern Sie so mühelos Ihre Datenpräsentation.
type: docs
weight: 110
url: /de/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Bietet Zugriff auf die Formatierungseigenschaften der Zeile.

```csharp
public RowFormat RowFormat { get; }
```

## Beispiele

Zeigt, wie die Formatierung einer Tabellenzeile geändert wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Verwenden Sie die Eigenschaft „RowFormat“ der ersten Zeile, um eine Formatierung festzulegen, die das Erscheinungsbild der gesamten Zeile ändert.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Zeigt, wie das Format von Zeilen und Zellen in einer Tabelle geändert wird.

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

// Verwenden Sie die Eigenschaft "RowFormat" der ersten Zeile, um die Formatierung zu ändern
// des Inhalts aller Zellen in dieser Zeile.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Verwenden Sie die Eigenschaft „CellFormat“ der ersten Zelle in der letzten Zeile, um die Formatierung des Inhalts dieser Zelle zu ändern.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Siehe auch

* class [RowFormat](../../rowformat/)
* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
