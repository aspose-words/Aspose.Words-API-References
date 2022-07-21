---
title: CellFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt alle Formatierungen für eine Tabellenzelle dar.
type: docs
weight: 5960
url: /de/net/aspose.words.tables/cellformat/
---
## CellFormat class

Stellt alle Formatierungen für eine Tabellenzelle dar.

```csharp
public class CellFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders) { get; } | Ruft eine Sammlung von Rahmen der Zelle ab. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding) { get; set; } | Gibt den Abstand (in Punkt) zurück oder legt ihn fest, der unter dem Inhalt der Zelle hinzugefügt werden soll. |
| [FitText](../../aspose.words.tables/cellformat/fittext) { get; set; } | Wenn wahr, passt Text in die Zelle und komprimiert jeden Absatz auf die Breite der Zelle. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge) { get; set; } | Gibt an, wie die Zelle horizontal mit anderen Zellen in der Zeile verbunden wird. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding) { get; set; } | Gibt den Abstand (in Punkten) zurück oder legt ihn fest, der links vom Inhalt der Zelle hinzugefügt werden soll. |
| [Orientation](../../aspose.words.tables/cellformat/orientation) { get; set; } | Gibt die Textausrichtung in einer Tabellenzelle zurück oder legt sie fest. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth) { get; set; } | Gibt die bevorzugte Breite der Zelle zurück oder legt sie fest. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding) { get; set; } | Gibt den Abstand (in Punkten) zurück oder legt ihn fest, der rechts vom Inhalt der Zelle hinzugefügt werden soll. |
| [Shading](../../aspose.words.tables/cellformat/shading) { get; } | Gibt ein Shading-Objekt zurück, das sich auf die Schattierungsformatierung für die Zelle bezieht. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding) { get; set; } | Gibt den Abstand (in Punkten) zurück oder legt ihn fest, der über dem Inhalt der Zelle hinzugefügt werden soll. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment) { get; set; } | Gibt die vertikale Ausrichtung des Textes in der Zelle zurück oder legt sie fest. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge) { get; set; } | Gibt an, wie die Zelle vertikal mit anderen Zellen verbunden wird. |
| [Width](../../aspose.words.tables/cellformat/width) { get; set; } | Ruft die Breite der Zelle in Punkten ab. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext) { get; set; } | Wenn wahr, Text für die Zelle umbrechen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting)() | Setzt auf Standardzellenformatierung zurück. Ändert nicht die Breite der Zelle. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings)(double, double, double, double) | Legt den Abstand (in Punkten) fest, der links/oben/rechts/unten vom Inhalt der Zelle hinzugefügt werden soll. |

### Beispiele

Zeigt, wie die Formatierung einer Tabellenzelle geändert wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Verwenden Sie die "CellFormat"-Eigenschaft einer Zelle, um eine Formatierung festzulegen, die das Erscheinungsbild dieser Zelle ändert.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
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

* namensraum [Aspose.Words.Tables](../../aspose.words.tables)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
