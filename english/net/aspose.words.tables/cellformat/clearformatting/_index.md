---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
second_title: Aspose.Words for .NET API Reference
description: CellFormat ClearFormatting method. Resets to default cell formatting. Does not change the width of the cell in C#.
type: docs
weight: 150
url: /net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Resets to default cell formatting. Does not change the width of the cell.

```csharp
public void ClearFormatting()
```

## Examples

Shows how to combine the rows from two tables into one.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 -  Using the "GetChild" method:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Append all rows from the current table to the next.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Remove the empty table container.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### See Also

* class [CellFormat](../)
* namespace [Aspose.Words.Tables](../../cellformat/)
* assembly [Aspose.Words](../../../)
