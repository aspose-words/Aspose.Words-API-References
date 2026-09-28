---
title: DocumentProperty.link_source property
linktitle: link_source property
articleTitle: link_source property
second_title: Aspose.Words for Python
description: "DocumentProperty.link_source property. Gets the source of a linked custom document property."
type: docs
weight: 20
url: /zh/python-net/aspose.words.properties/documentproperty/link_source/
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
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
builder.write('Hello world!')
builder.end_bookmark('MyBookmark')
# 将新自定义属性链接到书签。此属性的值
# 将是它在 "LinkSource" 成员中引用的书签内容。
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

