---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Tables.AutoFitBehavior, um die Größenänderung von Tabellen mit der AutoFit-Methode zu optimieren und so das Layout und die Präsentation von Dokumenten zu verbessern.
type: docs
weight: 7080
url: /de/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Bestimmt, wie Aspose.Words die Größe der Tabelle ändert, wenn Sie die[`AutoFit`](../table/autofit/) Methode.

```csharp
public enum AutoFitBehavior
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words aktiviert die Option „AutoFit“, entfernt die bevorzugte Breite aus der Tabelle und allen Zellen und aktualisiert dann das Tabellenlayout. |
| AutoFitToWindow | `1` | Wenn Sie diesen Wert verwenden, aktiviert Aspose.Words die Option „AutoFit“, legt die bevorzugte Breite für die Tabelle auf 100 % fest, entfernt die bevorzugten Breiten aus allen Zellen und aktualisiert dann das Tabellenlayout. |
| FixedColumnWidths | `2` | Aspose.Words deaktiviert die AutoFit-Option und entfernt die bevorzugte Breite aus der Tabelle. |

## Beispiele

Zeigt, wie beim Anwenden eines Stils eine neue Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Wir müssen mindestens eine Zeile einfügen, bevor wir eine Tabellenformatierung festlegen.
builder.InsertCell();

// Legen Sie den verwendeten Tabellenstil basierend auf der Stilkennung fest.
// Beachten Sie, dass beim Speichern im DOC-Format nicht alle Tabellenstile verfügbar sind.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Wenden Sie den Stil teilweise auf Funktionen der Tabelle basierend auf Prädikaten an und erstellen Sie dann die Tabelle.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

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

* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
