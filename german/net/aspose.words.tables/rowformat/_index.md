---
title: Class RowFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Tables.RowFormat klas. Stellt alle Formatierungen für eine Tabellenzeile dar.
type: docs
weight: 6030
url: /de/net/aspose.words.tables/rowformat/
---
## RowFormat class

Stellt alle Formatierungen für eine Tabellenzeile dar.

```csharp
public class RowFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | Wahr, wenn der Text in einer Tabellenzeile über einen Seitenumbruch geteilt werden darf. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | Ruft die Sammlung von Standardzellenrahmen für die Zeile ab. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | Wahr, wenn die Zeile als Tabellenüberschrift auf jeder Seite wiederholt wird, wenn die Tabelle mehr als eine Seite umfasst. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | Holt oder setzt die Höhe der Tabellenzeile in Punkt. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | Ruft die Regel zur Bestimmung der Höhe der Tabellenzeile ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | Setzt auf Standard-Zeilenformatierung zurück. |

### Beispiele

Zeigt, wie die Formatierung einer Tabellenzeile geändert wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Verwenden Sie die "RowFormat"-Eigenschaft der ersten Zeile, um eine Formatierung festzulegen, die das Erscheinungsbild dieser gesamten Zeile ändert.
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

// Verwenden Sie die "RowFormat"-Eigenschaft der ersten Zeile, um die Formatierung zu ändern
// des Inhalts aller Zellen in dieser Zeile.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Verwenden Sie die Eigenschaft "CellFormat" der ersten Zelle in der letzten Zeile, um die Formatierung des Inhalts dieser Zelle zu ändern.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

Zeigt, wie eine Tabelle mit benutzerdefinierten Rahmen erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen Dokumentersteller
// wendet sie auf jede Zeile und Zelle an, die wir damit hinzufügen.
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

// Wenn Sie die Formatierung ändern, wird sie auf die aktuelle Zelle angewendet,
// und alle neuen Zellen, die wir danach mit dem Builder erstellen.
// Dies wirkt sich nicht auf die zuvor hinzugefügten Zellen aus.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Erhöhen Sie die Zeilenhöhe, um sie an den vertikalen Text anzupassen.
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

### Siehe auch

* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)


