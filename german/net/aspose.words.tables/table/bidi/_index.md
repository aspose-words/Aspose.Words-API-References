---
title: Table.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words für .NET
description: Entdecken Sie die Bidi-Eigenschaften für Tabellen für eine nahtlose Formatierung von rechts nach links. Verbessern Sie Ihr Webdesign mit einfachen Anpassungsoptionen!
type: docs
weight: 80
url: /de/net/aspose.words.tables/table/bidi/
---
## Table.Bidi property

Ruft ab oder legt fest, ob es sich um eine von rechts nach links verlaufende Tabelle handelt.

```csharp
public bool Bidi { get; set; }
```

## Bemerkungen

Wann`WAHR`, die Zellen in dieser Zeile werden von rechts nach links angeordnet.

Der Standardwert ist`FALSCH`.

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

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
