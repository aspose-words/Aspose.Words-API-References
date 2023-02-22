---
title: Class RevisionGroupCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.RevisionGroupCollection klass. En samling avRevisionGroup objekt som representerar revisionsgrupper i dokumentet.
type: docs
weight: 4530
url: /sv/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

En samling av[`RevisionGroup`](../revisiongroup/) objekt som representerar revisionsgrupper i dokumentet.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Returnerar antalet revisionsgrupper i samlingen. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Returnerar en revisionsgrupp vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt. |

### Anmärkningar

Du skapar inte instanser av den här klassen direkt. Använd[`Groups`](../revisioncollection/groups/) egenskap för att få versionsgrupper närvarande i ett dokument.

### Exempel

Visar hur man får en grupp av revisioner i ett dokument.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


