---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /ru/python-net/aspose.words.lists/listformat/list_level_number/
---

## ListFormat.list_level_number property

Gets or sets the list level number (0 to 8) for the paragraph.


```python
@property
def list_level_number(self) -> int:
    ...

@list_level_number.setter
def list_level_number(self, value: int):
    ...

```

### Remarks

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [ListFormat.list](../list/) property is set to reference a valid list.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# Список позволяет нам организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
# Мы можем создавать вложенные списки, увеличивая уровень отступа.
# Мы можем начать и завершить список, используя свойство "ListFormat" объекта DocumentBuilder.
# Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
# Ниже представлены два типа списков, которые мы можем создать с помощью Document Builder.
# 1 -  Маркированный список:
# Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Завершите маркированный список.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  Нумерованный список:
# Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.list_format.apply_number_default()
# Этот абзац — первый элемент. Первый элемент нумерованного списка будет иметь символ "1.".
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# Вызовите метод "ListIndent", чтобы увеличить текущий уровень списка,
# что начнёт новый самостоятельный список с более глубоким отступом у текущего элемента первого уровня списка.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Это первые три элемента списка второго уровня, которые будут сохранять счётчик
# независимый от счётчика первого уровня списка. В соответствии с текущим форматом списка,
# они будут иметь символы "a.", "b." и "c.".
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# Вызовите метод "ListOutdent", чтобы вернуться к предыдущему уровню списка.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Эти два абзаца продолжат счётчик первого уровня списка.
# Эти элементы будут иметь символы "2." и "3."
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Если мы увеличим уровень списка до уровня, к которому ранее уже добавляли элементы,
# вложенный список будет отдельным от предыдущего, и его нумерация начнётся с начала.
# Эти элементы списка будут иметь символы "a.", "b.", "c.", "d.", и "e".
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Снова уменьшите отступ уровня списка.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Завершите нумерованный список.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

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

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)

