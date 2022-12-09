---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Retrieves a Run at the given index.
type: docs
weight: 27
url: /cpp/aspose.words/runcollection/idx_get/
---
## RunCollection::idx_get method


Retrieves a [Run](../../run/) at the given index.

```cpp
System::SharedPtr<Aspose::Words::Run> Aspose::Words::RunCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples



Shows how to determine the revision type of an inline node. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revision runs.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.Words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to change the proposed change effectively.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
auto run = System::DynamicCast<Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

SharedPtr<Paragraph> firstParagraph = run->get_ParentParagraph();
SharedPtr<RunCollection> runs = firstParagraph->get_Runs();

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

* Class [Run](../../run/)
* Class [RunCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
