---
title: TableStyle.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words per .NET
description: Scopri la proprietà TableStyle LeftIndent per personalizzare facilmente il rientro sinistro della tua tabella, per un controllo migliore del layout e un impatto visivo migliore.
type: docs
weight: 90
url: /it/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

Ottiene o imposta il valore che rappresenta il rientro sinistro di una tabella.

```csharp
public double LeftIndent { get; set; }
```

## Esempi

Mostra come impostare la posizione di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due metodi per allineare una tabella orizzontalmente.
// 1 - Utilizza la proprietà "Allineamento" per allinearlo a una posizione sulla pagina, ad esempio al centro:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Inseriamo una tabella e applichiamo lo stile che abbiamo creato.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Utilizzare "LeftIndent" per specificare un rientro dal margine sinistro della pagina:
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

* class [TableStyle](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
