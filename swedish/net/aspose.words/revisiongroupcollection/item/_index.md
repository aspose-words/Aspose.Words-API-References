---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkelt åtkomst till specifika revisionsgrupper med egenskapen RevisionGroupCollection Item. Förbättra din datahantering med exakt indexering.
type: docs
weight: 20
url: /sv/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Returnerar en revisionsgrupp vid det angivna indexet.

```csharp
public RevisionGroup this[int index] { get; }
```

## Exempel

Visar hur man hämtar en grupp revisioner i ett dokument.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Se även

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
