---
title: StartTrackRevisions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 690
url: /net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#1}

Starts automatically marking all further changes you make to the document programmatically as revision changes.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [`DocumentBuilder`](../../documentbuilder)

This method does not change the [`TrackRevisions`](../trackrevisions) option and does not use its value for the purposes of revision tracking.

### Examples

Shows how to track revisions while editing a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Stop tracking revisions to not count any future edits as revisions.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.MinValue when we start tracking revisions.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// We can accept/reject these revisions programmatically
// by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### See Also

* method [StopTrackRevisions](../stoptrackrevisions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#2}

Starts automatically marking all further changes you make to the document programmatically as revision changes.

```csharp
public void StartTrackRevisions(string author)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | String | Initials of the author to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [`DocumentBuilder`](../../documentbuilder)

This method does not change the [`TrackRevisions`](../trackrevisions) option and does not use its value for the purposes of revision tracking.

### Examples

Shows how to track revisions while editing a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Stop tracking revisions to not count any future edits as revisions.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.MinValue when we start tracking revisions.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// We can accept/reject these revisions programmatically
// by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### See Also

* method [StopTrackRevisions](../stoptrackrevisions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
