---
title: ListLevel.text_position property
linktitle: text_position property
articleTitle: text_position property
second_title: Aspose.Words for Python
description: "ListLevel.text_position property. Returns or sets the position (in points) for the second line of wrapping text for the list level."
type: docs
weight: 130
url: /ru/python-net/aspose.words.lists/listlevel/text_position/
---

## ListLevel.text_position property

Returns or sets the position (in points) for the second line of wrapping text for the list level.


```python
@property
def text_position(self) -> float:
    ...

@text_position.setter
def text_position(self, value: float):
    ...

```

### Remarks

[ListLevel.text_position](./) corresponds to LeftIndent of the paragraph.




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

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)
* property [ListLevel.number_position](../number_position/)
* property [ListLevel.tab_position](../tab_position/)

