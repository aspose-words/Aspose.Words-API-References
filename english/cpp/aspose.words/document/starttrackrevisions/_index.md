---
title: StartTrackRevisions
second_title: Aspose.Words for C++ API Reference
description: Starts automatically marking all further changes you make to the document programmatically as revision changes.
type: docs
weight: 1184
url: /cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Starts automatically marking all further changes you make to the document programmatically as revision changes.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Parameter | Type | Description |
| --- | --- | --- |
| author | const System::String\& | Initials of the author to use for revisions. |
## Remarks


If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../documentbuilder/)

This method does not change the [TrackRevisions](../get_trackrevisions/) option and does not use its value for the purposes of revision tracking.

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
* Library [Aspose.Words](../../../)
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Starts automatically marking all further changes you make to the document programmatically as revision changes.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| author | const System::String\& | Initials of the author to use for revisions. |
| dateTime | System::DateTime | The date and time to use for revisions. |
## Remarks


If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../documentbuilder/)

This method does not change the [TrackRevisions](../get_trackrevisions/) option and does not use its value for the purposes of revision tracking.

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
* Library [Aspose.Words](../../../)
