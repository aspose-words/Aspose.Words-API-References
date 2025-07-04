---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words for .NET
description: Discover the OriginalLoadFormat property to easily access the format of the original document loaded into your object, enhancing document management.
type: docs
weight: 310
url: /net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Gets the format of the original document that was loaded into this object.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Remarks

If you created a new blank document, returns the Doc value.

## Examples

Shows how to retrieve details of a document's load operation.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.That(doc.OriginalFileName, Is.EqualTo(MyDir + "Document.docx"));
Assert.That(doc.OriginalLoadFormat, Is.EqualTo(LoadFormat.Docx));
```

### See Also

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
