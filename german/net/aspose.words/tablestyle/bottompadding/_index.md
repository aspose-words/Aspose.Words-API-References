---
title: TableStyle.BottomPadding
second_title: Aspose.Words für .NET-API-Referenz
description: TableStyle eigendom. Ruft den Abstand in Punkten ab der unterhalb des Inhalts von Tabellenzellen hinzugefügt werden soll oder legt diesen fest.
type: docs
weight: 50
url: /de/net/aspose.words/tablestyle/bottompadding/
---
## TableStyle.BottomPadding property

Ruft den Abstand (in Punkten) ab, der unterhalb des Inhalts von Tabellenzellen hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double BottomPadding { get; set; }
```

### Beispiele

Zeigt, wie Sie benutzerdefinierte Stileinstellungen für die Tabelle erstellen.

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
* namensraum [Aspose.Words](../../tablestyle/)
* Montage [Aspose.Words](../../../)


