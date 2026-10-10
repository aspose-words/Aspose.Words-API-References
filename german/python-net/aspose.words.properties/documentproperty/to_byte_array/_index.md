---
title: DocumentProperty.to_byte_array method
linktitle: to_byte_array method
articleTitle: to_byte_array method
second_title: Aspose.Words for Python
description: "DocumentProperty.to_byte_array method. Returns the property value as byte array."
type: docs
weight: 70
url: /de/python-net/aspose.words.properties/documentproperty/to_byte_array/
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
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Wenn wir ein Dokument speichern, dessen "Thumbnail"-Eigenschaft Bilddaten enthält, die wir hinzugefügt haben, als Epub,
# kann ein Reader, der dieses Dokument öffnet, das Bild vor der ersten Seite anzeigen.
properties = doc.built_in_document_properties
thumbnail_bytes = system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Logo.jpg')
properties.thumbnail = thumbnail_bytes
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Thumbnail.epub')
# Wir können das Thumbnail-Bild eines Dokuments extrahieren und im lokalen Dateisystem speichern.
thumbnail = doc.built_in_document_properties.get_by_name('Thumbnail')
system_helper.io.File.write_all_bytes(ARTIFACTS_DIR + 'DocumentProperties.Thumbnail.gif', thumbnail.to_byte_array())
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

