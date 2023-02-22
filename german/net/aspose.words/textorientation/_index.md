---
title: Enum TextOrientation
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.TextOrientation opsomming. Gibt die Textausrichtung auf einer Seite in einer Tabellenzelle oder einem Textrahmen an.
type: docs
weight: 6130
url: /de/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Gibt die Textausrichtung auf einer Seite, in einer Tabellenzelle oder einem Textrahmen an.

```csharp
public enum TextOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | `0` | Text wird horizontal angeordnet (lr-tb). |
| Downward | `1` | Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl). |
| Upward | `3` | Text wird um 90 Grad nach links gedreht, sodass er von unten nach oben erscheint (bt-lr). |
| HorizontalRotatedFarEast | `4` | Text wird horizontal angeordnet, aber fernöstliche Zeichen werden um 90 Grad nach links gedreht (lr-tb-v). |
| VerticalFarEast | `5` | Fernöstliche Zeichen werden vertikal angezeigt, anderer Text wird um 90 Grad nach rechts gedreht, um von oben nach unten angezeigt zu werden (tb-rl-v). |
| VerticalRotatedFarEast | `7` | Fernöstliche Zeichen werden vertikal angezeigt, anderer Text wird um 90 Grad nach rechts gedreht, um vertikal von oben nach unten und dann horizontal von links nach rechts angezeigt zu werden (tb-lr-v). |

### Beispiele

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

// Beim Erstellen der Tabelle wendet der Document Builder seine aktuellen RowFormat/CellFormat-Eigenschaftswerte an
// zur aktuellen Zeile/Zelle, in der sich der Cursor befindet, und zu allen neuen Zeilen/Zellen, wenn sie erstellt werden.
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

// Zuvor hinzugefügte Zeilen und Zellen sind nicht rückwirkend von Änderungen an der Formatierung des Builders betroffen.
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


