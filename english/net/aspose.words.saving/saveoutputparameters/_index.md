---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Saving.SaveOutputParameters class, which provides essential details post-document save, enhancing your document management experience.
type: docs
weight: 6390
url: /net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation. The caller can use or ignore this object.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class SaveOutputParameters
```

## Properties

| Name | Description |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Returns the Content-Type string (Internet Media Type) that identifies the type of the saved document. |

## Examples

Shows how to access output parameters of a document's save operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.That(parameters.ContentType, Is.EqualTo("application/msword"));

// This property changes depending on the save format.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.That(parameters.ContentType, Is.EqualTo("application/pdf"));
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
