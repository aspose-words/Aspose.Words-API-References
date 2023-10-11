---
title: ConditionalStyleCollection.ClearFormatting
second_title: Aspose.Words für .NET-API-Referenz
description: ConditionalStyleCollection methode. Löscht alle bedingten Stile des Tabellenstils.
type: docs
weight: 150
url: /de/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Löscht alle bedingten Stile des Tabellenstils.

```csharp
public void ClearFormatting()
```

### Beispiele

Zeigt, wie bedingte Tabellenstile zurückgesetzt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Legen Sie den Tabellenstil fest, um die Ränder der ersten Zeile der Tabelle rot zu färben.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Legen Sie den Tabellenstil fest, um die Ränder der letzten Tabellenzeile blau zu färben.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Nachfolgend finden Sie zwei Möglichkeiten, die Methode „ClearFormatting“ zum Löschen der bedingten Stile zu verwenden.
// 1 – Bedingte Stile für einen bestimmten Teil einer Tabelle löschen:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 – Bedingte Stile für die gesamte Tabelle löschen:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Siehe auch

* class [ConditionalStyleCollection](../)
* namensraum [Aspose.Words](../../conditionalstylecollection/)
* Montage [Aspose.Words](../../../)


