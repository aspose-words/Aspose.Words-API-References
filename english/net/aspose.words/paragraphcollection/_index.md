---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.ParagraphCollection for seamless access to structured Paragraph nodes, enhancing document manipulation and efficiency in your projects.
type: docs
weight: 5130
url: /net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Provides typed access to a collection of [`Paragraph`](../paragraph/) nodes.

To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/net/working-with-paragraphs/) documentation article.

```csharp
public class ParagraphCollection : NodeCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Gets the number of nodes in the collection. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Retrieves a [`Paragraph`](../paragraph/) at the given index. (2 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determines whether a node is in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Provides a simple "foreach" style iteration over the collection of nodes. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Copies all paragraphs from the collection to a new array of paragraphs. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
