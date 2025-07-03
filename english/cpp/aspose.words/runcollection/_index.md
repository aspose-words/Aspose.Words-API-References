---
title: Aspose::Words::RunCollection class
linktitle: RunCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::RunCollection class. Provides typed access to a collection of Run nodes. To learn more, visit the  documentation article in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words/runcollection/
---
## RunCollection class


Provides typed access to a collection of [Run](../run/) nodes. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class RunCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Run](../run/) at the given index. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all runs from the collection to a new array of runs. |
| static [Type](./type/)() |  |

## Examples



Shows how to determine the revision type of an inline node. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.Words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to change the proposed change effectively.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Below are five types of revisions that can flag an Inline node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  A "format" revision:
// This revision occurs when we change the formatting of text while tracking changes.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## See Also

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
