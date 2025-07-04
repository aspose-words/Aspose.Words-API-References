---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the Count property of RevisionGroupCollection. Easily retrieve the total number of revision groups, enhancing your data management efficiency.
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

Assert.That(doc.Revisions.Groups.Count, Is.EqualTo(7));

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### See Also

* class [RevisionGroupCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
