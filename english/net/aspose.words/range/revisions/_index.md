---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words for .NET
description: Discover Range Revisions, Track and manage property changes effortlessly with our comprehensive collection of revisions for enhanced project clarity.
type: docs
weight: 40
url: /net/aspose.words/range/revisions/
---
## Range.Revisions property

Gets a collection of revisions (tracked changes) that exist in this range.

```csharp
public RevisionCollection Revisions { get; }
```

## Remarks

The returned collection is a "live" collection, which means if you remove parts of a document that contain revisions, the deleted revisions will automatically disappear from this collection.

## Examples

Shows how to work with revisions in range.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Reject the first section revisions.
doc.FirstSection.Range.Revisions.RejectAll();
```

### See Also

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
