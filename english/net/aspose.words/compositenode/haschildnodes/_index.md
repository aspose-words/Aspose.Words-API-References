---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words for .NET
description: CompositeNode HasChildNodes property. Returns true if this node has any child nodes in C#.
type: docs
weight: 30
url: /net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Returns `true` if this node has any child nodes.

```csharp
public bool HasChildNodes { get; }
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

* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
