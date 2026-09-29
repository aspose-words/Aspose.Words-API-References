---
title: List.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for Python
description: "List.style property. Gets the list style that this list references or defines."
type: docs
weight: 80
url: /ru/python-net/aspose.words.lists/list/style/
---

## List.style property

Gets the list style that this list references or defines.


```python
@property
def style(self) -> aspose.words.Style:
    ...

```

### Remarks

If this list is not associated with a list style, the property will return ``None``.

A list could be a reference to a list style, in this case [List.is_list_style_reference](../is_list_style_reference/)
will be ``True``.

A list could be a definition of a list style, in this case [List.is_list_style_definition](../is_list_style_definition/)
will be ``True``. Such a list cannot be applied to paragraphs in the document directly.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# Список позволяет нам организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
# Мы можем создавать вложенные списки, увеличивая уровень отступа.
# Мы можем начать и завершить список, используя свойство "ListFormat" объекта DocumentBuilder.
# Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
# Мы можем включить целый объект List в стиль.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Измените внешний вид всех уровней списка в нашем списке.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Создайте другой список из списка внутри стиля.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Добавьте несколько элементов списка, которые наш список отформатирует.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Создайте и примените другой список, основанный на стиле списка.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)

