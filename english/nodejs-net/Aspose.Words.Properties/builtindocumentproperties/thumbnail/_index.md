---
title: BuiltInDocumentProperties.thumbnail property
linktitle: thumbnail property
articleTitle: thumbnail property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.thumbnail property. Gets or sets the thumbnail of the document."
type: docs
weight: 290
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/thumbnail/
---

## BuiltInDocumentProperties.thumbnail property

Gets or sets the thumbnail of the document.




```js
get thumbnail(): number[]
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Thrown if the image is invalid or its format is unsupported for specific format of document. |

### Remarks

For now this property is used only when a document is being exported to ePub,
it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export.

Only gif, jpeg and png images can be used for ePub publication.




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
* class [BuiltInDocumentProperties](../)

