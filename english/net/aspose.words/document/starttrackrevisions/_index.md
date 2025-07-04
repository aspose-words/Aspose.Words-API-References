---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words for .NET
description: Effortlessly track document changes with the StartTrackRevisions method. Automatically mark all edits as revisions for seamless collaboration and clarity.
type: docs
weight: 760
url: /net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Starts automatically marking all further changes you make to the document programmatically as revision changes.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |

## Remarks

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [`DocumentBuilder`](../../documentbuilder/)

This method does not change the [`TrackRevisions`](../trackrevisions/) option and does not use its value for the purposes of revision tracking.

## Examples

Shows how to track revisions while editing a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder.Write("Hello world! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(0));
Assert.That(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision, Is.False);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(1));
Assert.That(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision, Is.True);
Assert.That(doc.Revisions[0].Author, Is.EqualTo("John Doe"));
Assert.That((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10, Is.True);

// Stop tracking revisions to not count any future edits as revisions.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(1));
Assert.That(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision, Is.False);

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.MinValue when we start tracking revisions.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(2));
Assert.That(doc.Revisions[1].Author, Is.EqualTo("John Doe"));
Assert.That(doc.Revisions[1].DateTime, Is.EqualTo(DateTime.MinValue));

// We can accept/reject these revisions programmatically
// by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### See Also

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Starts automatically marking all further changes you make to the document programmatically as revision changes.

```csharp
public void StartTrackRevisions(string author)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | String | Initials of the author to use for revisions. |

## Remarks

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [`DocumentBuilder`](../../documentbuilder/)

This method does not change the [`TrackRevisions`](../trackrevisions/) option and does not use its value for the purposes of revision tracking.

## Examples

Shows how to track revisions while editing a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder.Write("Hello world! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(0));
Assert.That(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision, Is.False);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(1));
Assert.That(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision, Is.True);
Assert.That(doc.Revisions[0].Author, Is.EqualTo("John Doe"));
Assert.That((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10, Is.True);

// Stop tracking revisions to not count any future edits as revisions.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(1));
Assert.That(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision, Is.False);

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.MinValue when we start tracking revisions.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.That(doc.Revisions.Count, Is.EqualTo(2));
Assert.That(doc.Revisions[1].Author, Is.EqualTo("John Doe"));
Assert.That(doc.Revisions[1].DateTime, Is.EqualTo(DateTime.MinValue));

// We can accept/reject these revisions programmatically
// by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### See Also

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
