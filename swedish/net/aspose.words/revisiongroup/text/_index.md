---
title: RevisionGroup.Text
second_title: Aspose.Words för .NET API Referens
description: RevisionGroup fast egendom. Returnerar infogat/raderad/flyttad text eller beskrivning av formatändring.
type: docs
weight: 30
url: /sv/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Returnerar infogat/raderad/flyttad text eller beskrivning av formatändring.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* namnutrymme [Aspose.Words](../../revisiongroup/)
* hopsättning [Aspose.Words](../../../)


