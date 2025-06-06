---
title: Table.CellSpacing
linktitle: CellSpacing
articleTitle: CellSpacing
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Table CellSpacing“, um den Zellenabstand in Punkten einfach anzupassen und so das Erscheinungsbild und die Lesbarkeit Ihrer Tabelle zu verbessern.
type: docs
weight: 100
url: /de/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

Ruft den Abstand (in Punkten) zwischen den Zellen ab oder legt ihn fest.

```csharp
public double CellSpacing { get; set; }
```

## Beispiele

Zeigt, wie Sie den Abstand zwischen einzelnen Zellen in einer Tabelle aktivieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Setzen Sie die Eigenschaft „AllowCellSpacing“ auf „true“, um den Abstand zwischen den Zellen zu ermöglichen
// mit einer Größe, die dem Wert der Eigenschaft „CellSpacing“ in Punkten entspricht.
// Setzen Sie die Eigenschaft „AllowCellSpacing“ auf „false“, um den Zellenabstand zu deaktivieren
// und ignorieren Sie den Wert der Eigenschaft „CellSpacing“.
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Durch Anpassen der Eigenschaft „CellSpacing“ wird der Zellenabstand automatisch aktiviert.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

Zeigt, wie benutzerdefinierte Stileinstellungen für die Tabelle erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Das Festlegen der Stileigenschaften einer Tabelle kann sich auf die Eigenschaften der Tabelle selbst auswirken.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
