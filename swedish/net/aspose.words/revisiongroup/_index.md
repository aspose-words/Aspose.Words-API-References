---
title: Class RevisionGroup
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.RevisionGroup klass. Representerar en grupp av sekventiellaRevision objekt.
type: docs
weight: 4780
url: /sv/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Representerar en grupp av sekventiella[`Revision`](../revision/) objekt.

För att lära dig mer, besök[Spåra ändringar i ett dokument](https://docs.aspose.com/words/net/track-changes-in-a-document/) dokumentationsartikel.

```csharp
public class RevisionGroup
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Hämtar författaren till denna versionsgrupp. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Hämtar typen av revisioner som ingår i denna grupp. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Returnerar infogat/raderad/flyttad text eller beskrivning av formatändring. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


