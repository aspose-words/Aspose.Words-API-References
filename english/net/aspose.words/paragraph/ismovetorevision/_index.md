---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words for .NET
description: Discover the IsMoveToRevision property in Microsoft Word! Learn how it tracks changes and enhances your document editing experience.
type: docs
weight: 140
url: /net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Returns `true` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

```csharp
public bool IsMoveToRevision { get; }
```

## Examples

Shows how to check whether a paragraph is a move revision.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// This document contains "Move" revisions, which appear when we highlight text with the cursor,
// and then drag it to move it to another location
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
Assert.That(doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving), Is.EqualTo(6));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Move revisions consist of pairs of "Move from", and "Move to" revisions. 
// These revisions are potential changes to the document that we can either accept or reject.
// Before we accept/reject a move revision, the document
// must keep track of both the departure and arrival destinations of the text.
// The second and the fourth paragraph define one such revision, and thus both have the same contents.
Assert.That(paragraphs[3].GetText(), Is.EqualTo(paragraphs[1].GetText()));

// The "Move from" revision is the paragraph where we dragged the text from.
// If we accept the revision, this paragraph will disappear,
// and the other will remain and no longer be a revision.
Assert.That(paragraphs[1].IsMoveFromRevision, Is.True);

// The "Move to" revision is the paragraph where we dragged the text to.
// If we reject the revision, this paragraph instead will disappear, and the other will remain.
Assert.That(paragraphs[3].IsMoveToRevision, Is.True);
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
