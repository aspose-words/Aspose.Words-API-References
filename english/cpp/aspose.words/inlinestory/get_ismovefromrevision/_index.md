---
title: Aspose::Words::InlineStory::get_IsMoveFromRevision method
linktitle: get_IsMoveFromRevision
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::InlineStory::get_IsMoveFromRevision method. Returns true if this object was moved (deleted) in Microsoft Word while change tracking was enabled in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/inlinestory/get_ismovefromrevision/
---
## InlineStory::get_IsMoveFromRevision method


Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

```cpp
bool Aspose::Words::InlineStory::get_IsMoveFromRevision()
```


## Examples



Shows how to view revision-related properties of [InlineStory](../) nodes. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revision footnotes.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.Words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to undo and discard the proposed change.
ASSERT_TRUE(doc->get_HasRevisions());

SharedPtr<System::Collections::Generic::List<SharedPtr<Footnote>>> footnotes =
    doc->GetChildNodes(NodeType::Footnote, true)->LINQ_Cast<SharedPtr<Footnote>>()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Below are five types of revisions that can flag an InlineStory node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## See Also

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
