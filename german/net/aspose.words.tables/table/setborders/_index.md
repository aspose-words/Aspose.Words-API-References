---
title: Table.SetBorders
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Setzt alle Tabellenränder auf den angegebenen Linienstil die angegebene Breite und die angegebene Farbe.
type: docs
weight: 440
url: /de/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Setzt alle Tabellenränder auf den angegebenen Linienstil, die angegebene Breite und die angegebene Farbe.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| lineStyle | LineStyle | Der anzuwendende Linienstil. |
| lineWidth | Double | Die festzulegende Linienbreite (in Punkt). |
| color | Color | Die für den Rand zu verwendende Farbe. |

### Beispiele

Zeigt, wie alle Ränder einer Tabelle gleichzeitig formatiert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Alle vorhandenen Ränder aus der Tabelle löschen.
table.ClearBorders();

// Legen Sie eine einzelne grüne Linie fest, die als äußerer und innerer Rand dieser Tabelle dient.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Zeigt, wie Sie beim Erstellen einer Tabelle Rahmen- und Schattierungsfarben anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Tabelle starten und eine Standardfarbe/-stärke für ihre Ränder festlegen.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Erstelle eine Zeile mit zwei Zellen mit unterschiedlichen Hintergrundfarben.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Zellenformatierung zurücksetzen, um die Hintergrundfarben zu deaktivieren
// Legen Sie eine benutzerdefinierte Rahmenstärke für alle neuen Zellen fest, die vom Builder erstellt wurden.
// dann baue eine zweite Reihe.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Siehe auch

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


