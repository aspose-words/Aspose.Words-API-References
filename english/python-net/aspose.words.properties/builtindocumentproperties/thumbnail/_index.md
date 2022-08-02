---
title: thumbnail property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the thumbnail of the document."
type: docs
weight: 280
url: /python-net/aspose.words.properties/builtindocumentproperties/thumbnail/
---

## BuiltInDocumentProperties.thumbnail property

Gets or sets the thumbnail of the document.



For now this property is used only when a document is being exported to ePub,
it's not read from and written to other document formats.

Image of arbitrary format can be set to this property, but the format is checked during export.
System.InvalidOperationException is thrown if the image is invalid or its format is unsupported for
specific format of document.

Only gif, jpeg and png images can be used for ePub publication.




### Examples

Shows how to add a thumbnail to a document that we save as an Epub.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# If we save a document, whose "thumbnail" property contains image data that we added, as an Epub,
# a reader that opens that document may display the image before the first page.
properties = doc.built_in_document_properties

with open(IMAGE_DIR + "Logo.jpg", "rb") as file:
    thumbnail_bytes = file.read()

properties.thumbnail = thumbnail_bytes

doc.save(ARTIFACTS_DIR + "DocumentProperties.thumbnail.epub")

# We can extract a document's thumbnail image and save it to the local file system.
thumbnail = doc.built_in_document_properties.get_by_name("Thumbnail")

with open(ARTIFACTS_DIR + "DocumentProperties.thumbnail.gif", "wb") as file:
    file.write(thumbnail.to_byte_array())
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

