---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: Discover the RevisionGroup Author property to easily identify the author of each revision group, enhancing your document management efficiency.
type: docs
weight: 10
url: /net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Gets the author of this revision group.

```csharp
public string Author { get; }
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
