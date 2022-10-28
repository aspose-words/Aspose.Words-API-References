---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Retrieves a Paragraph at the given index.
type: docs
weight: 1
url: /cpp/aspose.words/paragraphcollection/idx_get/
---
## ParagraphCollection.idx_get method


Retrieves a **Paragraph** at the given index.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::ParagraphCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples




Shows how to check whether a paragraph is a move revision. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revisions.docx");

// This document contains "Move" revisions, which appear when we highlight text with the cursor,
// and then drag it to move it to another location
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count([](SharedPtr<Revision> r) { return r->get_RevisionType() == RevisionType::Moving; }));

SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Move revisions consist of pairs of "Move from", and "Move to" revisions.
// These revisions are potential changes to the document that we can either accept or reject.
// Before we accept/reject a move revision, the document
// must keep track of both the departure and arrival destinations of the text.
// The second and the fourth paragraph define one such revision, and thus both have the same contents.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// The "Move from" revision is the paragraph where we dragged the text from.
// If we accept the revision, this paragraph will disappear,
// and the other will remain and no longer be a revision.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// The "Move to" revision is the paragraph where we dragged the text to.
// If we reject the revision, this paragraph instead will disappear, and the other will remain.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

