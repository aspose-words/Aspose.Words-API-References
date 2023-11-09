---
title: DocumentProperty.link_source property
linktitle: link_source property
articleTitle: link_source property
second_title: Aspose.Words for Python
description: "DocumentProperty.link_source property. Gets the source of a linked custom document property."
type: docs
weight: 20
url: /python-net/aspose.words.properties/documentproperty/link_source/
---

## DocumentProperty.link_source property

Gets the source of a linked custom document property.


```python
@property
def link_source(self) -> str:
    ...

```

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
* class [DocumentProperty](../)

