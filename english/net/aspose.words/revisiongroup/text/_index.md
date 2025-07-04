---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Explore the RevisionGroup Text property to access inserted, deleted, or moved text, enhancing your document's formatting insights and editing efficiency.
type: docs
weight: 30
url: /net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Returns inserted/deleted/moved text or description of format change.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
