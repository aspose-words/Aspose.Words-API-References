---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.TextOrientation, um die Textausrichtung in Tabellenzellen und Textrahmen einfach zu steuern und so die Präsentation und Lesbarkeit von Dokumenten zu verbessern.
type: docs
weight: 7280
url: /de/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Gibt die Ausrichtung des Textes auf einer Seite, in einer Tabellenzelle oder einem Textrahmen an.

```csharp
public enum TextOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | `0` | Der Text ist horizontal angeordnet (lr-tb). |
| Downward | `1` | Der Text wird um 90 Grad nach rechts gedreht, um von oben nach unten (tb-rl) angezeigt zu werden. |
| Upward | `3` | Der Text wird um 90 Grad nach links gedreht, um von unten nach oben (bt-lr) angezeigt zu werden. |
| HorizontalRotatedFarEast | `4` | Der Text ist horizontal angeordnet, fernöstliche Zeichen sind jedoch um 90 Grad nach links gedreht (lr-tb-v). |
| VerticalFarEast | `5` | Fernöstliche Zeichen werden vertikal angezeigt, anderer Text wird um 90 Grad nach rechts gedreht, um von oben nach unten angezeigt zu werden (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Fernöstliche Zeichen werden vertikal angezeigt, anderer Text wird um 90 Grad nach rechts gedreht, um vertikal von oben nach unten und dann horizontal von links nach rechts (tb-lr-v) angezeigt zu werden. |

## Beispiele

Zeigt, wie eine formatierte 2x2-Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Beim Erstellen der Tabelle wendet der Dokumentgenerator seine aktuellen RowFormat/CellFormat-Eigenschaftswerte an
// zur aktuellen Zeile/Zelle, in der sich der Cursor befindet, und zu allen neuen Zeilen/Zellen, sobald diese erstellt werden.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Zuvor hinzugefügte Zeilen und Zellen werden durch Änderungen an der Formatierung des Builders nicht rückwirkend beeinflusst.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
