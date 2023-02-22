---
title: RevisionGroup.RevisionType
second_title: Aspose.Words för .NET API Referens
description: RevisionGroup fast egendom. Hämtar typen av revisioner som ingår i denna grupp.
type: docs
weight: 20
url: /sv/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Hämtar typen av revisioner som ingår i denna grupp.

```csharp
public RevisionType RevisionType { get; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../revisiongroup/)
* hopsättning [Aspose.Words](../../../)


