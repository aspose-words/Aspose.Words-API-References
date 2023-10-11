---
title: NodeCollection.IndexOf
second_title: Aspose.Words för .NET API Referens
description: NodeCollection metod. Returnerar det nollbaserade indexet för den angivna noden.
type: docs
weight: 70
url: /sv/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Returnerar det nollbaserade indexet för den angivna noden.

```csharp
public int IndexOf(Node node)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| node | Node | Noden att lokalisera. |

### Returvärde

Det nollbaserade indexet för noden inom samlingen, om det hittas; annars -1.

### Anmärkningar

Denna metod utför en linjär sökning; därför är den genomsnittliga exekveringstiden proportionell mot[`Count`](../count/).

### Exempel

Visar hur man hämtar indexet för en nod i en samling.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### Se även

* class [Node](../../node/)
* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../nodecollection/)
* hopsättning [Aspose.Words](../../../)


