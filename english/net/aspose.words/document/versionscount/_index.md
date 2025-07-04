---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words for .NET
description: Discover the Document VersionsCount property to easily track the number of stored document versions in your DOC files for better management and organization.
type: docs
weight: 480
url: /net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Gets the number of document versions that was stored in the DOC document.

```csharp
public int VersionsCount { get; }
```

## Remarks

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports versions only for DOC files.

This property allows to detect if there were document versions stored in this document before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions. If you save this document using Aspose.Words, the document will be saved without versions.

## Examples

Shows how to work with the versions count feature of older Microsoft Word documents.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// We can read this property of a document, but we cannot preserve it while saving.
Assert.That(doc.VersionsCount, Is.EqualTo(4));

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.That(doc.VersionsCount, Is.EqualTo(0));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
