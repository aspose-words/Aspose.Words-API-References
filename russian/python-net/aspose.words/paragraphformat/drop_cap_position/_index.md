---
title: ParagraphFormat.drop_cap_position property
linktitle: drop_cap_position property
articleTitle: drop_cap_position property
second_title: Aspose.Words for Python
description: "ParagraphFormat.drop_cap_position property. Gets or sets the position for a drop cap text."
type: docs
weight: 100
url: /ru/python-net/aspose.words/paragraphformat/drop_cap_position/
---

## ParagraphFormat.drop_cap_position property

Gets or sets the position for a drop cap text.


```python
@property
def drop_cap_position(self) -> aspose.words.DropCapPosition:
    ...

@drop_cap_position.setter
def drop_cap_position(self, value: aspose.words.DropCapPosition):
    ...

```

### Examples

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Список позволяет нам организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
# Мы можем создавать вложенные списки, увеличивая уровень отступа.
# Мы можем начать и завершить список, используя свойство "ListFormat" объекта DocumentBuilder.
# Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
# Создайте контурный список для заголовков.
outline_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 1')
# Создайте нумерованный список.
numbered_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Numbered list item 1.')
# Каждый абзац, составляющий список, будет иметь этот флаг.
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)
# Создайте маркированный список.
bulleted_list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln('Bulleted list item 1.')
builder.writeln('Bulleted list item 2.')
builder.paragraph_format.clear_formatting()
# Вернитесь к нумерованному списку.
builder.list_format.list = numbered_list
builder.writeln('Numbered list item 2.')
builder.writeln('Numbered list item 3.')
# Вернитесь к контурному списку.
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 2')
builder.paragraph_format.clear_formatting()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.NestedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

