---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.RevisionGroupCollection class. A collection of RevisionGroup objects that represent revision groups in the document in C#.
type: docs
weight: 4610
url: /net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

A collection of [`RevisionGroup`](../revisiongroup/) objects that represent revision groups in the document.

To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/net/track-changes-in-a-document/) documentation article.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Returns the number of revision groups in the collection. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Returns a revision group at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Returns an enumerator object. |

## Remarks

You do not create instances of this class directly. Use the [`Groups`](../revisioncollection/groups/) property to get revision groups present in a document.

## Examples

Shows how to get a group of revisions in a document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

Shows how to print info about a group of revisions in a document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### See Also

* class [RevisionGroup](../revisiongroup/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
