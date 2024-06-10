---
title: DocumentProperty.is_link_to_content property
linktitle: is_link_to_content property
articleTitle: is_link_to_content property
second_title: Aspose.Words for Python
description: "DocumentProperty.is_link_to_content property. Shows whether this property is linked to content or not."
type: docs
weight: 10
url: /python-net/aspose.words.properties/documentproperty/is_link_to_content/
---

## DocumentProperty.is_link_to_content property

Shows whether this property is linked to content or not.


```python
@property
def is_link_to_content(self) -> bool:
    ...

```

### Examples

Shows how to link a custom document property to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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
* class [DocumentProperty](../)

