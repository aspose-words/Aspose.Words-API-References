---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.RunCollection class for seamless access to Run nodes. Enhance your document processing with powerful, typed features!
type: docs
weight: 5560
url: /net/aspose.words/runcollection/
---
## RunCollection class

Provides typed access to a collection of [`Run`](../run/) nodes.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class RunCollection : NodeCollection
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Gets the number of nodes in the collection. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Retrieves a [`Run`](../run/) at the given index. (2 indexers) |

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
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Copies all runs from the collection to a new array of runs. (2 methods) |

## Examples

Shows how to determine the revision type of an inline node.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.Words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to change the proposed change effectively.
Assert.That(doc.Revisions.Count, Is.EqualTo(6));

// The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.That(runs.ToArray().Length, Is.EqualTo(6));

// Below are five types of revisions that can flag an Inline node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
Assert.That(runs[2].IsInsertRevision, Is.True);

// 2 -  A "format" revision:
// This revision occurs when we change the formatting of text while tracking changes.
Assert.That(runs[2].IsFormatRevision, Is.True);

// 3 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
Assert.That(runs[4].IsMoveFromRevision, Is.True);

// 4 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
Assert.That(runs[1].IsMoveToRevision, Is.True);

// 5 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
Assert.That(runs[5].IsDeleteRevision, Is.True);
```

### See Also

* class [NodeCollection](../nodecollection/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
