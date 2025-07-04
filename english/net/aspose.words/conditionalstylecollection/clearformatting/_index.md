---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: Discover how the ConditionalStyleCollection ClearFormatting method effectively removes all conditional styles from your table, enhancing clarity and design.
type: docs
weight: 150
url: /net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Clears all conditional styles of the table style.

```csharp
public void ClearFormatting()
```

## Examples

Shows how to reset conditional table styles.

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

// Set the table style to color the borders of the first row of the table in red.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Set the table style to color the borders of the last row of the table in blue.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// Below are two ways of using the "ClearFormatting" method to clear the conditional styles.
// 1 -  Clear the conditional styles for a specific part of a table:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.That(tableStyle.ConditionalStyles.FirstRow.Borders.Color, Is.EqualTo(Color.Empty));

// 2 -  Clear the conditional styles for the entire table:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.That(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty), Is.True);
```

### See Also

* class [ConditionalStyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
