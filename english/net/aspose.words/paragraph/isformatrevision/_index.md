---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words for .NET
description: Discover how the IsFormatRevision property in Microsoft Word tracks formatting changes, ensuring accurate document edits and enhanced collaboration.
type: docs
weight: 90
url: /net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.

```csharp
public bool IsFormatRevision { get; }
```

## Examples

Shows how to check whether a paragraph is a format revision.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// This paragraph is a "Format" revision, which occurs when we change the formatting of existing text
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
Assert.That(doc.FirstSection.Body.FirstParagraph.IsFormatRevision, Is.True);
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
