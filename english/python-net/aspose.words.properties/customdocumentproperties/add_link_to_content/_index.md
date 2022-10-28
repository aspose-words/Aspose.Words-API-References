---
title: add_link_to_content method
second_title: Aspose.Words for Python via .NET API Reference
description: "Creates a new linked to content custom document property."
type: docs
weight: 30
url: /python-net/aspose.words.properties/customdocumentproperties/add_link_to_content/
---

## add_link_to_content(name, link_source) {#str_str}

Creates a new linked to content custom document property.


```python
def add_link_to_content(self, name: str, link_source: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str |  |
| link_source | str |  |

### Returns

The newly created property object or ``None`` when the  is invalid.


### Examples

Shows how to link a custom document property to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.start_bookmark("MyBookmark")
builder.write("Hello world!")
builder.end_bookmark("MyBookmark")

# Link a new custom property to a bookmark. The value of this property
# will be the contents of the bookmark that it references in the "link_source" member.
custom_properties = doc.custom_document_properties
custom_property = custom_properties.add_link_to_content("Bookmark", "MyBookmark")

self.assertEqual(True, custom_property.is_link_to_content)
self.assertEqual("MyBookmark", custom_property.link_source)
self.assertEqual("Hello world!", custom_property.value)

doc.save(ARTIFACTS_DIR + "DocumentProperties.link_custom_document_properties_to_bookmark.docx")
```

### See Also

* module [aspose.words.properties](../../)
* class [CustomDocumentProperties](../)

