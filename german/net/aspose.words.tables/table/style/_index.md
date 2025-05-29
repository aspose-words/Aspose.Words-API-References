---
title: Table.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie das Erscheinungsbild Ihrer Tabelle mit der Eigenschaft „Tabellenstil“ ganz einfach anpassen können – werten Sie Ihre Designs mühelos mit einzigartigen Stilen auf!
type: docs
weight: 270
url: /de/net/aspose.words.tables/table/style/
---
## Table.Style property

Ruft den auf diese Tabelle angewendeten Tabellenstil ab oder legt ihn fest.

```csharp
public Style Style { get; set; }
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

* class [Style](../../../aspose.words/style/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
