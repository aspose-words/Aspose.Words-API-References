---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
second_title: Aspose.Words for .NET API Reference
description: BuiltInDocumentProperties Thumbnail property. Gets or sets the thumbnail of the document in C#.
type: docs
weight: 280
url: /net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Gets or sets the thumbnail of the document.

```csharp
public byte[] Thumbnail { get; set; }
```

## Remarks

For now this property is used only when a document is being exported to ePub, it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export. InvalidOperationException is thrown if the image is invalid or its format is unsupported for specific format of document.

Only gif, jpeg and png images can be used for ePub publication.

## Examples

Shows how to add a thumbnail to a document that we save as an Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// If we save a document, whose "Thumbnail" property contains image data that we added, as an Epub,
// a reader that opens that document may display the image before the first page.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// We can extract a document's thumbnail image and save it to the local file system.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../builtindocumentproperties/)
* assembly [Aspose.Words](../../../)
