---
title: CustomDocumentProperties.add_link_to_content method
linktitle: add_link_to_content method
articleTitle: add_link_to_content method
second_title: Aspose.Words for Python
description: "CustomDocumentProperties.add_link_to_content method. Creates a new linked to content custom document property."
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
| name | str | The name of the property. |
| link_source | str | The source of the property. |

### Returns

The newly created property object or ``None`` when the *linkSource* is invalid.


### Examples

Shows how to link a custom document property to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
builder.write('Hello world!')
builder.end_bookmark('MyBookmark')
# Link a new custom property to a bookmark. The value of this property
# will be the contents of the bookmark that it references in the "LinkSource" member.
custom_properties = doc.custom_document_properties
custom_property = custom_properties.add_link_to_content('Bookmark', 'MyBookmark')
self.assertEqual(True, custom_property.is_link_to_content)
self.assertEqual('MyBookmark', custom_property.link_source)
self.assertEqual('Hello world!', custom_property.value)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [CustomDocumentProperties](../)

