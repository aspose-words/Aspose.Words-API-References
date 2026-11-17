---
title: Aspose::Words::RevisionCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::RevisionCollection::get_Count method. Returns the number of revisions in the collection in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/revisioncollection/get_count/
---
## RevisionCollection::get_Count method


Returns the number of revisions in the collection.

```cpp
int32_t Aspose::Words::RevisionCollection::get_Count()
```

## Examples


Shows how to work with revisions in a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normal editing of the document does not count as a revision.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// To register our edits as revisions, we need to declare an author, and then start tracking them.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(doc->get_Revisions()->get_Count(), 1);

// This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
// The "StartTrackRevisions" method does not affect its value,
// and the document is tracking revisions programmatically despite it having a value of "false".
// If we open this document using Microsoft Word, it will not be tracking revisions.
ASSERT_FALSE(doc->get_TrackRevisions());

// We have added text using the document builder, so the first revision is an insertion-type revision.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(revision->get_Author(), u"John Doe");
ASSERT_EQ(revision->get_ParentNode()->GetText(), u"This is revision #1. ");
ASSERT_EQ(revision->get_RevisionType(), RevisionType::Insertion);
ASSERT_EQ(System::DateTime::get_Now().get_Date(), revision->get_DateTime().get_Date());
ASPOSE_ASSERT_EQ(revision->get_Group(), doc->get_Revisions()->get_Groups()->idx_get(0));

// Remove a run to create a deletion-type revision.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Adding a new revision places it at the beginning of the revision collection.
ASSERT_EQ(doc->get_Revisions()->idx_get(0)->get_RevisionType(), RevisionType::Deletion);
ASSERT_EQ(doc->get_Revisions()->get_Count(), 2);

// Insert revisions show up in the document body even before we accept/reject the revision.
// Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
// also linger in the document until we accept the revision.
ASSERT_EQ(doc->GetText().Trim(), u"This does not count as a revision. This is revision #1.");

// Accepting the delete revision will remove its parent node from the paragraph text
// and then remove the collection's revision itself.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(doc->get_Revisions()->get_Count(), 1);
ASSERT_EQ(doc->GetText().Trim(), u"This is revision #1.");

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Now move the node to create a moving revision type.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(doc->get_Revisions()->idx_get(0)->get_RevisionType(), RevisionType::Moving);
ASSERT_EQ(doc->get_Revisions()->get_Count(), 8);
ASSERT_EQ(doc->GetText().Trim(), u"This is revision #2.\rThis is revision #1. \rThis is revision #2.");

// The moving revision is now at index 1. Reject the revision to discard its contents.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(doc->get_Revisions()->get_Count(), 6);
ASSERT_EQ(doc->GetText().Trim(), u"This is revision #1. \rThis is revision #2.");
```
## See Also

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
