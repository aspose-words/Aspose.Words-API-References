---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words för .NET
description: CompositeNode HasChildNodes fast egendom. ReturnerarSann om denna nod har några undernoder i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Returnerar`Sann` om denna nod har några undernoder.

```csharp
public bool HasChildNodes { get; }
```

## Exempel

Visar hur man kombinerar raderna från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan finns två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tables" för en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Med "GetChild"-metoden:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägg till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma bordsbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Se även

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
