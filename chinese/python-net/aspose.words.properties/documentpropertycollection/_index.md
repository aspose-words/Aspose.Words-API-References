---
title: DocumentPropertyCollection class
linktitle: DocumentPropertyCollection class
articleTitle: DocumentPropertyCollection class
second_title: Aspose.Words for Python
description: "aspose.words.properties.DocumentPropertyCollection class. Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections"
type: docs
weight: 40
url: /zh/python-net/aspose.words.properties/documentpropertycollection/
---

## DocumentPropertyCollection class

Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/python-net/work-with-document-properties/) documentation article.




### Remarks

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [DocumentProperty](../documentproperty/) object by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets number of items in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all properties from the collection. |
|[ contains(name)](./contains/#str) | Returns ``True`` if a property with the specified name exists in the collection. |
|[ get_by_name(name)](./get_by_name/#str) | Returns a [DocumentProperty](../documentproperty/) object by the name of the property. |
|[ index_of(name)](./index_of/#str) | Gets the index of a property by name. |
|[ remove(name)](./remove/#str) | Removes a property with the specified name from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a property at the specified index. |

### Examples

Shows how to work with a document's custom properties.

```python
import datetime
import aspose.words as aw
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# 自定义文档属性是我们可以添加到文档的键值对。
properties.add(name='Authorized', value=True)
properties.add(name='Authorized By', value='John Doe')
properties.add(name='Authorized Date', value=datetime.date.today())
properties.add(name='Authorized Revision', value=doc.built_in_document_properties.revision_number)
properties.add(name='Authorized Amount', value=123.45)
# 该集合按字母顺序对自定义属性进行排序。
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# 打印文档中的每个自定义属性。
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# 使用 DOCPROPERTY 字段显示自定义属性的值。
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code=' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# 我们可以在 Microsoft Word 中通过 “File” -> “Properties” > “Advanced Properties” > “Custom” 找到这些自定义属性。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.DocumentPropertyCollection.docx')
# 下面是从文档中删除自定义属性的三种方法。
# 1 -  按索引删除：
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  按名称删除：
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  一次性清空整个集合：
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.properties](../)
* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)

