---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words for .NET
description: Discover the SaveOutputParameters ContentType property, which provides the Internet Media Type for your saved documents, ensuring accurate file identification.
type: docs
weight: 10
url: /net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document.

```csharp
public string ContentType { get; }
```

## Examples

Shows how to access output parameters of a document's save operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// This property changes depending on the save format.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### See Also

* class [SaveOutputParameters](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
