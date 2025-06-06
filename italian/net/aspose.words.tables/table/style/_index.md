---
title: Table.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words per .NET
description: Scopri come personalizzare facilmente l'aspetto della tua tabella con la proprietà Stile tabella arricchisci i tuoi progetti con stili unici senza sforzo!
type: docs
weight: 270
url: /it/net/aspose.words.tables/table/style/
---
## Table.Style property

Ottiene o imposta lo stile tabella applicato a questa tabella.

```csharp
public Style Style { get; set; }
```

## Esempi

Mostra come creare impostazioni di stile personalizzate per la tabella.

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

// L'impostazione delle proprietà di stile di una tabella può influire sulle proprietà della tabella stessa.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Guarda anche

* class [Style](../../../aspose.words/style/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
