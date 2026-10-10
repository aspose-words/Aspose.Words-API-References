---
title: DocumentProperty.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "DocumentProperty.value property. Gets or sets the value of the property."
type: docs
weight: 50
url: /zh/python-net/aspose.words.properties/documentproperty/value/
---

## DocumentProperty.value property

Gets or sets the value of the property.


```python
@property
def value(self) -> object:
    ...

@value.setter
def value(self, value: object):
    ...

```

### Remarks

Cannot be ``None``.




### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
# “Document” 对象在其成员中包含部分元数据。
print(f'Document filename:\n\t "{doc.original_file_name}"')
# 文档还在其内置属性中存储元数据。
# 每个内置属性都是文档的 “BuiltInDocumentProperties” 对象的成员。
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # 某些属性可能存储多个值。
    if isinstance(doc_property.value, (list, tuple)):
        for value in doc_property.value:
            print(f'\tValue:\t"{value}"')
    else:
        print(f'\tValue:\t"{doc_property.value}"')
```

### See Also

* module [aspose.words.properties](../../)
* class [DocumentProperty](../)

