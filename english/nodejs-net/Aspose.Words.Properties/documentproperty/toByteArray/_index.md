---
title: DocumentProperty.toByteArray method
linktitle: toByteArray method
articleTitle: toByteArray method
second_title: Aspose.Words for NodeJs
description: "DocumentProperty.toByteArray method. Returns the property value as byte array."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Properties/documentproperty/toByteArray/
---

## toByteArray() {#default}

Returns the property value as byte array.


```js
toByteArray()
```

### Remarks

Throws an exception if the property type is not [PropertyType.ByteArray](../../propertytype/#ByteArray).




### Examples

Shows how to add a thumbnail to a document that we save as an Epub.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// If we save a document, whose "Thumbnail" property contains image data that we added, as an Epub,
// a reader that opens that document may display the image before the first page.
let properties = doc.builtInDocumentProperties;

let thumbnailBytes = base.loadFileToArray(base.imageDir + "Logo.jpg");
properties.thumbnail = thumbnailBytes;

doc.save(base.artifactsDir + "DocumentProperties.thumbnail.epub");

// We can extract a document's thumbnail image and save it to the local file system.
let thumbnail = doc.builtInDocumentProperties.thumbnail;
fs.writeFileSync(base.artifactsDir + "DocumentProperties.thumbnail.gif", Buffer.from(thumbnail));
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [DocumentProperty](../)

