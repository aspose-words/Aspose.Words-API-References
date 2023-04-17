---
title: Aspose::Words::Document::StopTrackRevisions method
linktitle: StopTrackRevisions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::StopTrackRevisions method. Stops automatic marking of document changes as revisions in C++.'
type: docs
weight: 93000
url: /cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


Stops automatic marking of document changes as revisions.

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## Examples



Shows how to track revisions while editing a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_LE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds(), 10);

// Stop tracking revisions to not count any future edits as revisions.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.MinValue when we start tracking revisions.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// We can accept/reject these revisions programmatically
// by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc->Save(ArtifactsDir + u"Document.StartTrackRevisions.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
