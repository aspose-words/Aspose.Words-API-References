---
title: TableStyle.Alignment
second_title: Aspose.Words per .NET API Reference
description: TableStyle proprietà. Specifica lallineamento per lo stile della tabella.
type: docs
weight: 10
url: /it/net/aspose.words/tablestyle/alignment/
---
## TableStyle.Alignment property

Specifica l'allineamento per lo stile della tabella.

```csharp
public TableAlignment Alignment { get; set; }
```

### Osservazioni

Il valore predefinito èLeft .

### Esempi

Mostra come impostare la posizione di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per allineare una tabella orizzontalmente.
// 1 - Usa la proprietà "Allineamento" per allinearlo a una posizione sulla pagina, come il centro:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Inserisci una tabella e applica ad essa lo stile che abbiamo creato.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Usa "LeftIndent" per specificare un rientro dal margine sinistro della pagina:
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

### Guarda anche

* enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* class [TableStyle](../)
* spazio dei nomi [Aspose.Words](../../tablestyle/)
* assemblea [Aspose.Words](../../../)


