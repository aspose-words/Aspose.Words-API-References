---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words for .NET
description: Discover the Paragraph IsInsertRevision property in Word. Learn how it identifies inserted text during change tracking for efficient document management.
type: docs
weight: 110
url: /net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

```csharp
public bool IsInsertRevision { get; }
```

## Examples

Shows how to work with revision paragraphs.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// The above paragraphs are not revisions.
// Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.That(para.IsInsertRevision, Is.True);

// Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.That(paragraphs.Count, Is.EqualTo(4));

para = paragraphs[2];
para.Remove();

// Such paragraphs will remain until we either accept or reject the delete revision.
// Accepting the revision will remove the paragraph for good,
// and rejecting the revision will leave it in the document as if we never deleted it.
Assert.That(paragraphs.Count, Is.EqualTo(4));
Assert.That(para.IsDeleteRevision, Is.True);

// Accept the revision, and then verify that the paragraph is gone.
doc.AcceptAllRevisions();

Assert.That(paragraphs.Count, Is.EqualTo(3));
Assert.That(para.Count, Is.EqualTo(0));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4."));
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
