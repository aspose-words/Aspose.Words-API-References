---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words för .NET
description: ConditionalStyleCollection ClearFormatting metod. Rensar alla villkorliga stilar i tabellstilen i C#.
type: docs
weight: 150
url: /sv/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Rensar alla villkorliga stilar i tabellstilen.

```csharp
public void ClearFormatting()
```

## Exempel

Visar hur man återställer villkorliga tabellstilar.

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

// Ställ in tabellstilen för att färga kanterna på den första raden i tabellen i rött.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Ställ in tabellstilen för att färga kanterna på den sista raden i tabellen i blått.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Nedan finns två sätt att använda "ClearFormatting"-metoden för att rensa de villkorliga stilarna.
// 1 - Rensa de villkorliga stilarna för en specifik del av en tabell:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Rensa de villkorliga stilarna för hela tabellen:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Se även

* class [ConditionalStyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
