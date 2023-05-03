---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
second_title: Aspose.Words for .NET API Reference
description: DocumentProperty ToByteArray method. Returns the property value as byte array in C#.
type: docs
weight: 70
url: /net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Returns the property value as byte array.

```csharp
public byte[] ToByteArray()
```

## Remarks

Throws an exception if the property type is not ByteArray.

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

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../documentproperty/)
* assembly [Aspose.Words](../../../)
