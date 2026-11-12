---
title: CustomXmlSchemaCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "CustomXmlSchemaCollection.clear method. Removes all elements from the collection."
type: docs
weight: 40
url: /ru/python-net/aspose.words.markup/customxmlschemacollection/clear/
---

## clear() {#default}

Removes all elements from the collection.


```python
def clear(self):
    ...
```

### Examples

Shows how to work with an XML schema collection.

```python
doc = aw.Document()
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Hello, World!</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
# Добавьте ассоциацию XML‑схемы.
xml_part.schemas.add('http://www.w3.org/2001/XMLSchema')
# Клонируйте коллекцию ассоциаций XML‑схем пользовательской части XML,
# а затем добавьте несколько новых схем в клон.
schemas = xml_part.schemas.clone()
schemas.add('http://www.w3.org/2001/XMLSchema-instance')
schemas.add('http://schemas.microsoft.com/office/2006/metadata/contentType')
self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of('http://schemas.microsoft.com/office/2006/metadata/contentType'))
# Переберите схемы и выведите каждый элемент.
for schema in schemas:
    print(schema)
# Ниже представлены три способа удаления схем из коллекции.
# 1 - Удалить схему по индексу:
schemas.remove_at(2)
# 2 - Удалить схему по значению:
schemas.remove('http://www.w3.org/2001/XMLSchema')
# 3 - Использовать метод "Clear" для одновременного очистки коллекции.
schemas.clear()
self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

