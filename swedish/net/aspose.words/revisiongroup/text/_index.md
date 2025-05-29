---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Utforska egenskapen RevisionGroup Text för att komma åt infogat, borttaget eller flyttat text, vilket förbättrar dokumentets formateringsinsikter och redigeringseffektivitet.
type: docs
weight: 30
url: /sv/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Returnerar infogad/borttagen/flyttad text eller beskrivning av formatändring.

```csharp
public string Text { get; }
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
