---
title: ListFormat class
linktitle: ListFormat class
articleTitle: ListFormat class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListFormat class. Allows to control what list formatting is applied to a paragraph"
type: docs
weight: 30
url: /ru/python-net/aspose.words.lists/listformat/
---

## ListFormat class

Allows to control what list formatting is applied to a paragraph.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

A paragraph in a Microsoft Word document can be bulleted or numbered.
When a paragraph is bulleted or numbered, it is said that list formatting
is applied to the paragraph.

You do not create objects of the [ListFormat](./) class directly.
You access [ListFormat](./) as a property of another object that can
have list formatting associated with it. At the moment the objects that can
have list formatting are: [Paragraph](../../aspose.words/paragraph/),
[Style](../../aspose.words/style/) and [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies
what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable
to paragraph styles only) allows to specify what list formatting and list level
is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/)
provides access to the list formatting at the current cursor position
inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

The list formatting itself is stored inside a [List](../list/)
object that is stored separately from the paragraphs. The list objects
are stored inside a [ListCollection](../listcollection/) collection. There is a single
[ListCollection](../listcollection/) collection per [Document](../../aspose.words/document/).

The paragraphs do not physically belong to a list. The paragraphs just
reference a particular list object via the [ListFormat.list](./list/) property
and a particular level in the list via the [ListFormat.list_level_number](./list_level_number/) property.
By setting these two properties you control what bullets and numbering is
applied to a paragraph.




### Properties

| Name | Description |
| --- | --- |
| [is_list_item](./is_list_item/) | True when the paragraph has bulleted or numbered formatting applied to it. |
| [list](./list/) | Gets or sets the list this paragraph is a member of. |
| [list_level](./list_level/) | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [list_level_number](./list_level_number/) | Gets or sets the list level number (0 to 8) for the paragraph. |

### Methods

| Name | Description |
| --- | --- |
|[ apply_bullet_default()](./apply_bullet_default/#default) | Starts a new default bulleted list and applies it to the paragraph. |
|[ apply_number_default()](./apply_number_default/#default) | Starts a new default numbered list and applies it to the paragraph. |
|[ list_indent()](./list_indent/#default) | Increases the list level of the current paragraph by one level. |
|[ list_outdent()](./list_outdent/#default) | Decreases the list level of the current paragraph by one level. |
|[ remove_numbers()](./remove_numbers/#default) | Removes numbers or bullets from the current paragraph and sets list level to zero. |

### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Список позволяет нам организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
# Мы можем создавать вложенные списки, увеличивая уровень отступа.
# Мы можем начать и завершить список, используя свойство "ListFormat" объекта DocumentBuilder.
# Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
# Ниже представлены два типа списков, которые мы можем создать с помощью DocumentBuilder.
# 1 -  Нумерованный список:
# Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Устанавливая свойство "ListLevelNumber", мы можем увеличить уровень списка
# чтобы начать автономный подпункт в текущем элементе списка.
# Шаблон списка Microsoft Word под названием "NumberDefault" использует цифры для создания уровней списка на первом уровне.
# Более глубокие уровни списка используют буквы и римские цифры нижнего регистра.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Маркированный список:
# Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
# Более глубокие уровни этого списка будут использовать разные символы, такие как "■" и "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Мы можем отключить форматирование списка, чтобы последующие абзацы не форматировались как списки, сбросив флаг "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words.lists](../)

