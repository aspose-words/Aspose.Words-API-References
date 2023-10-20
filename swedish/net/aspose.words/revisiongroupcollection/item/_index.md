---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: RevisionGroupCollection Item fast egendom. Returnerar en revisionsgrupp vid det angivna indexet i C#.
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

Visar hur man får en grupp av revisioner i ett dokument.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Se även

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
