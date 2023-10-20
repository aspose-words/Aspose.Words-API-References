---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words för .NET
description: RevisionGroupCollection Count fast egendom. Returnerar antalet revisionsgrupper i samlingen i C#.
type: docs
weight: 10
url: /sv/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Returnerar antalet revisionsgrupper i samlingen.

```csharp
public int Count { get; }
```

## Exempel

Visar hur man skriver ut information om en grupp revisioner i ett dokument.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Se även

* class [RevisionGroupCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
