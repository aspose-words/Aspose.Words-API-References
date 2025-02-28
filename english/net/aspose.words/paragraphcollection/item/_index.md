---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access specific Paragraphs easily with the ParagraphCollection Item property. Retrieve any Paragraph by index for seamless text management.
type: docs
weight: 10
url: /net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

Retrieves a [`Paragraph`](../../paragraph/) at the given index.

```csharp
public Paragraph this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the collection. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples

Shows how to check whether a paragraph is a move revision.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// This document contains "Move" revisions, which appear when we highlight text with the cursor,
// and then drag it to move it to another location
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Move revisions consist of pairs of "Move from", and "Move to" revisions. 
// These revisions are potential changes to the document that we can either accept or reject.
// Before we accept/reject a move revision, the document
// must keep track of both the departure and arrival destinations of the text.
// The second and the fourth paragraph define one such revision, and thus both have the same contents.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// The "Move from" revision is the paragraph where we dragged the text from.
// If we accept the revision, this paragraph will disappear,
// and the other will remain and no longer be a revision.
Assert.True(paragraphs[1].IsMoveFromRevision);

// The "Move to" revision is the paragraph where we dragged the text to.
// If we reject the revision, this paragraph instead will disappear, and the other will remain.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### See Also

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
