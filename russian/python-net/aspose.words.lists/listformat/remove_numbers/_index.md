---
title: ListFormat.remove_numbers method
linktitle: remove_numbers method
articleTitle: remove_numbers method
second_title: Aspose.Words for Python
description: "ListFormat.remove_numbers method. Removes numbers or bullets from the current paragraph and sets list level to zero."
type: docs
weight: 90
url: /ru/python-net/aspose.words.lists/listformat/remove_numbers/
---

## remove_numbers() {#default}

Removes numbers or bullets from the current paragraph and sets list level to zero.


```python
def remove_numbers(self):
    ...
```

### Remarks

Calling this method is equivalent to setting the [ListFormat.list](../list/) property to ``None``.




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

Shows how to remove list formatting from all paragraphs in the main text of a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
for paragraph in paras:
    paragraph = paragraph.as_paragraph()
    paragraph.list_format.remove_numbers()
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

