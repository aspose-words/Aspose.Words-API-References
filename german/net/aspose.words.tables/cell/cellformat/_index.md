---
title: Cell.CellFormat
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die CellFormat-Eigenschaft von Cell, um einfach auf Zellenformatierungsoptionen zuzugreifen und diese anzupassen, um die Datenpräsentation in Ihren Anwendungen zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Bietet Zugriff auf die Formatierungseigenschaften der Zelle.

```csharp
public CellFormat CellFormat { get; }
```

## Beispiele

Zeigt, wie die Formatierung einer Tabellenzelle geändert wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Verwenden Sie die Eigenschaft „CellFormat“ einer Zelle, um eine Formatierung festzulegen, die das Erscheinungsbild dieser Zelle ändert.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Zeigt, wie die Zeilen aus zwei Tabellen zu einer kombiniert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Unten sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 – Aus der „Tabellen“-Sammlung eines Body-Knotens:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Verwenden der Methode „GetChild“:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Alle Zeilen der aktuellen Tabelle an die nächste anhängen.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Entfernen Sie den leeren Tabellencontainer.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
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

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
