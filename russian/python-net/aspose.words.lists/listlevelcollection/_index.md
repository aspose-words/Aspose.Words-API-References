---
title: ListLevelCollection class
linktitle: ListLevelCollection class
articleTitle: ListLevelCollection class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListLevelCollection class. A collection of list formatting for each level in a list"
type: docs
weight: 70
url: /ru/python-net/aspose.words.lists/listlevelcollection/
---

## ListLevelCollection class

A collection of list formatting for each level in a list.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a list level by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of levels in this list. |

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# Список позволяет нам организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
# Мы можем создавать вложенные списки, увеличивая уровень отступа.
# Мы можем начать и завершить список, используя свойство "ListFormat" объекта DocumentBuilder.
# Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
# Создайте список из шаблона Microsoft Word и настройте первые два уровня его списка.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# Это значение NumberFormat создаст звездчатые символы маркеров списка.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Создайте абзацы и примените к ним оба уровня нашего пользовательского форматирования списка.
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

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

* module [aspose.words.lists](../)

