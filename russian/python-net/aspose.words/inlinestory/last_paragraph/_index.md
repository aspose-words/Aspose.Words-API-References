---
title: InlineStory.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 70
url: /ru/python-net/aspose.words/inlinestory/last_paragraph/
---

## InlineStory.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# У узлов Table есть метод "EnsureMinimum()", который гарантирует, что таблица содержит хотя бы одну ячейку.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Мы можем разместить таблицу внутри сноски, и она появится в нижнем колонтитуле страницы, где делается ссылка.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# У InlineStory также есть метод "EnsureMinimum()", но в этом случае,
# он гарантирует, что последний дочерний элемент узла является абзацем,
# чтобы мы могли легко кликать и вводить текст в Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Отредактируйте внешний вид якоря, который представляет собой маленький верхний индекс
# в основном тексте, указывающий на сноску.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Все узлы inline story имеют свои соответствующие типы историй.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# Комментарий — это другой тип inline story.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# Родительским абзацем узла inline story будет абзац из основного тела документа.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Однако последний абзац — это абзац из содержимого текста комментария,
# который будет находиться за пределами основного тела документа в виде речевого пузыря.
# Комментарий по умолчанию не будет иметь дочерних узлов,
# поэтому мы можем применить метод EnsureMinimum() чтобы разместить здесь абзац также.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# Как только у нас появится абзац, мы можем переместить builder, выполнить это и написать наш комментарий.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

