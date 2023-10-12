---
title: TableStyle.LeftIndent
second_title: Aspose.Words für .NET-API-Referenz
description: TableStyle eigendom. Ruft den Wert ab der den linken Einzug einer Tabelle darstellt oder legt diesen fest.
type: docs
weight: 90
url: /de/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

Ruft den Wert ab, der den linken Einzug einer Tabelle darstellt, oder legt diesen fest.

```csharp
public double LeftIndent { get; set; }
```

### Beispiele

Zeigt, wie die Position einer Tabelle festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten, eine Tabelle horizontal auszurichten.
// 1 – Verwenden Sie die Eigenschaft „Alignment“, um es an einer Stelle auf der Seite auszurichten, beispielsweise in der Mitte:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Fügen Sie eine Tabelle ein und wenden Sie den von uns erstellten Stil darauf an.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 – Verwenden Sie „LeftIndent“, um einen Einzug vom linken Rand der Seite anzugeben:
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### Siehe auch

* class [TableStyle](../)
* namensraum [Aspose.Words](../../tablestyle/)
* Montage [Aspose.Words](../../../)


