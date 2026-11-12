---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /ru/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# У конструктора документа есть курсор, который выступает как часть документа
# куда конструктор добавляет новые узлы, когда мы используем его методы построения документа.
# Этот курсор работает так же, как мигающий курсор Microsoft Word,
# и он также всегда оказывается сразу после любого узла, который конструктор только что вставил.
# Чтобы добавить содержимое в другую часть документа,
# мы можем переместить курсор к другому узлу с помощью метода "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Курсор теперь находится перед узлом, к которому мы его переместили.
# Добавление второго фрагмента вставит его перед первым фрагментом.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Переместите курсор в конец документа, чтобы продолжить добавлять текст в конец, как и раньше.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

