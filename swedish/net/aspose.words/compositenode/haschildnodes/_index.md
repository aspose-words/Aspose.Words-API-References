---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words för .NET
description: Upptäck om en CompositeNode har underordnade noder med egenskapen HasChildNodes. Förenkla din kodning med denna viktiga funktion för effektiv nodhantering.
type: docs
weight: 30
url: /sv/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Returer`sann` om den här noden har några undernoder.

```csharp
public bool HasChildNodes { get; }
```

## Exempel

Visar hur man kombinerar rader från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan följer två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tabeller" i en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Använda metoden "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägger till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma tabellbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Se även

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
