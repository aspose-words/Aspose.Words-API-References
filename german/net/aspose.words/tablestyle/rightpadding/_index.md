---
title: TableStyle.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: Aspose.Words für .NET
description: Entdecken Sie die TableStyle RightPadding-Eigenschaft und passen Sie Ihr Tabellenzellenlayout mit präzisem Abstand für verbesserte Lesbarkeit und Präsentation an.
type: docs
weight: 110
url: /de/net/aspose.words/tablestyle/rightpadding/
---
## TableStyle.RightPadding property

Ruft den Abstand (in Punkten) ab, der rechts vom Inhalt der Tabellenzellen hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double RightPadding { get; set; }
```

## Beispiele

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

* class [TableStyle](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
