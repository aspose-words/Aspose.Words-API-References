---
title: DocumentProperty.to_byte_array method
linktitle: to_byte_array method
articleTitle: to_byte_array method
second_title: Aspose.Words for Python
description: "DocumentProperty.to_byte_array method. Returns the property value as byte array."
type: docs
weight: 70
url: /python-net/aspose.words.properties/documentproperty/to_byte_array/
---

## to_byte_array() {#default}

Returns the property value as byte array.


```python
def to_byte_array(self):
    ...
```

### Remarks

Throws an exception if the property type is not [PropertyType.BYTE_ARRAY](../../propertytype/#BYTE_ARRAY).




### Examples

Shows how to add a thumbnail to a document that we save as an Epub.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
# If we save a document, whose "thumbnail" property contains image data that we added, as an Epub,
# a reader that opens that document may display the image before the first page.
properties = doc.built_in_document_properties
with open(IMAGE_DIR + 'Logo.jpg', 'rb') as file:
    thumbnail_bytes = file.read()
properties.thumbnail = thumbnail_bytes
doc.save(ARTIFACTS_DIR + 'DocumentProperties.thumbnail.epub')
# We can extract a document's thumbnail image and save it to the local file system.
thumbnail = doc.built_in_document_properties.get_by_name('Thumbnail')
with open(ARTIFACTS_DIR + 'DocumentProperties.thumbnail.gif', 'wb') as file:
    file.write(thumbnail.to_byte_array())
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

