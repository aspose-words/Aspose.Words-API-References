---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RevisionGroup RevisionType för att enkelt identifiera och hantera typerna av revisioner i ditt projekt. Effektivisera ditt arbetsflöde idag!
type: docs
weight: 20
url: /sv/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Hämtar typen av revisioner som ingår i den här gruppen.

```csharp
public RevisionType RevisionType { get; }
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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
