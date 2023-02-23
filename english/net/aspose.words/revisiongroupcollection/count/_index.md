---
title: RevisionGroupCollection.Count
linktitle: Count
second_title: Aspose.Words for .NET API Reference
description: RevisionGroupCollection property. Returns the number of revision groups in the collection in C#.
type: docs
weight: 10
url: /net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Returns the number of revision groups in the collection.

```csharp
public int Count { get; }
```

## Examples

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

* class [RevisionGroupCollection](../)
* namespace [Aspose.Words](../../revisiongroupcollection/)
* assembly [Aspose.Words](../../../)
