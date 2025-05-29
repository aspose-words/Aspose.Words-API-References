---
title: TableStyle.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words per .NET
description: Scopri la proprietà TableStyle LeftPadding per personalizzare il layout delle celle della tua tabella. Regola facilmente la spaziatura a sinistra per un aspetto curato e professionale.
type: docs
weight: 100
url: /it/net/aspose.words/tablestyle/leftpadding/
---
## TableStyle.LeftPadding property

Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle della tabella.

```csharp
public double LeftPadding { get; set; }
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

* class [TableStyle](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
