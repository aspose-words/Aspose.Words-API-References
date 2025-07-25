---
title: Aspose::Words::Revision::get_Author method
linktitle: get_Author
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Revision::get_Author method. Gets or sets the author of this revision. Can not be empty string or null in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/revision/get_author/
---
## Revision::get_Author method


Gets or sets the author of this revision. Can not be empty string or **null**.

```cpp
System::String Aspose::Words::Revision::get_Author()
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
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
// The "StartTrackRevisions" method does not affect its value,
// and the document is tracking revisions programmatically despite it having a value of "false".
// If we open this document using Microsoft Word, it will not be tracking revisions.
ASSERT_FALSE(doc->get_TrackRevisions());

// We have added text using the document builder, so the first revision is an insertion-type revision.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Remove a run to create a deletion-type revision.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Adding a new revision places it at the beginning of the revision collection.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Insert revisions show up in the document body even before we accept/reject the revision.
// Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
// also linger in the document until we accept the revision.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Accepting the delete revision will remove its parent node from the paragraph text
// and then remove the collection's revision itself.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

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

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// The moving revision is now at index 1. Reject the revision to discard its contents.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## See Also

* Class [Revision](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
