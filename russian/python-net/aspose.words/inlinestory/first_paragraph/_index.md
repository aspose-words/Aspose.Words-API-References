---
title: InlineStory.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.first_paragraph property. Gets the first paragraph in the story."
type: docs
weight: 10
url: /ru/python-net/aspose.words/inlinestory/first_paragraph/
---

## InlineStory.first_paragraph property

Gets the first paragraph in the story.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Добавьте текст и сослаться на него сноской. Эта сноска разместит небольшой верхний индекс
# маркер после текста, на который она ссылается, и создаст запись под основным текстом внизу страницы.
# Эта запись будет содержать маркер ссылки сноски и текст ссылки,
# которые мы передадим методу "InsertFootnote" построителя документа.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Если это свойство установлено в "true", то маркер ссылки нашей сноски
# будет её индексом среди всех сносок раздела.
# Это первая сноска, поэтому маркер ссылки будет "1".
self.assertTrue(footnote.is_auto)
# Мы можем переместить построитель документа внутрь сноски, чтобы отредактировать её текст ссылки.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Мы можем задать пользовательский маркер ссылки, который сноска будет использовать вместо её индексного номера.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Закладка с установленным флагом "IsAuto", равным true, всё равно будет показывать свой реальный индекс
# даже если предыдущие закладки отображают пользовательские метки ссылок, то метка ссылки этой закладки будет "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'JD', date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write('Comment text.')
self.assertEqual(date.today(), comment.date_time.date())
# В Microsoft Word мы можем щёлкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него.
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

