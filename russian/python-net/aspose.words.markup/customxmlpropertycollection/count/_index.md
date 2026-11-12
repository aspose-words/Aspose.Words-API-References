---
title: CustomXmlPropertyCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "CustomXmlPropertyCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /ru/python-net/aspose.words.markup/customxmlpropertycollection/count/
---

## CustomXmlPropertyCollection.count property

Gets the number of elements contained in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Smart tags.doc')
# Смарт‑тег появляется в документе, когда Microsoft Word распознаёт часть его текста как некоторый тип данных,
# например, имя, дату или адрес, и преобразует его в гиперссылку, отображающуюся пурпурным пунктирным подчеркиванием.
# В Word 2003 мы можем включить смарт-теги через "Tools" -> "AutoCorrect options..." -> "SmartTags".
# В нашем входном документе есть три объекта, которые Microsoft Word зарегистрировал как смарт-теги.
# Смарт-теги могут быть вложенными, поэтому эта коллекция содержит больше.
smart_tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_smart_tag(), b), list(doc.get_child_nodes(aw.NodeType.SMART_TAG, True)))))
self.assertEqual(8, len(smart_tags))
# Член "Properties" смарт-тега содержит его метаданные, которые будут различаться для каждого типа смарт-тега.
# Свойства смарт-тега типа "date" содержат его год, месяц и день.
properties = smart_tags[7].properties
self.assertEqual(4, properties.count)
for current in properties:
    print(f'Property name: {current.name}, value: {current.value}')
    self.assertEqual('', current.uri)
# Мы также можем получать доступ к свойствам различными способами, например в виде пары ключ‑значение.
self.assertTrue(properties.contains('Day'))
self.assertEqual('22', properties.get_by_name('Day').value)
self.assertEqual('2003', properties[2].value)
self.assertEqual(1, properties.index_of_key('Month'))
# Ниже представлены три способа удаления элементов из коллекции свойств.
# 1 -  Удалить по индексу:
properties.remove_at(3)
self.assertEqual(3, properties.count)
# 2 -  Удалить по имени:
properties.remove('Year')
self.assertEqual(2, properties.count)
# 3 -  Очистить всю коллекцию сразу:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPropertyCollection](../)

