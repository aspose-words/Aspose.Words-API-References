---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.RevisionGroup class, designed to efficiently manage and organize sequential Revision objects for streamlined document editing.
type: docs
weight: 5510
url: /net/aspose.words/revisiongroup/
---
## RevisionGroup class

Represents a group of sequential [`Revision`](../revision/) objects.

To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/net/track-changes-in-a-document/) documentation article.

```csharp
public class RevisionGroup
```

## Properties

| Name | Description |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Gets the author of this revision group. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Gets the type of revisions included in this group. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Returns inserted/deleted/moved text or description of format change. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
