---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RevisionGroup Author för att enkelt identifiera författaren till varje revisionsgrupp, vilket förbättrar effektiviteten i din dokumenthantering.
type: docs
weight: 10
url: /sv/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Hämtar författaren till denna revisionsgrupp.

```csharp
public string Author { get; }
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

* class [RevisionGroup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
