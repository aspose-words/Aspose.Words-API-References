---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words för .NET
description: Upptäck hur metoden ConditionalStyleCollection ClearFormatting effektivt tar bort alla villkorsstyrda format från din tabell, vilket förbättrar tydlighet och design.
type: docs
weight: 150
url: /sv/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Rensar alla villkorsstyrda format i tabellformatet.

```csharp
public void ClearFormatting()
```

## Exempel

Visar hur man återställer villkorliga tabellformat.

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

// Ställ in tabellstilen så att kanterna på den sista raden i tabellen färgas blått.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Nedan följer två sätt att använda metoden "ClearFormatting" för att rensa de villkorliga formaten.
// 1 - Rensa de villkorliga formaten för en specifik del av en tabell:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Rensa de villkorliga formaten för hela tabellen:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Se även

* class [ConditionalStyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
