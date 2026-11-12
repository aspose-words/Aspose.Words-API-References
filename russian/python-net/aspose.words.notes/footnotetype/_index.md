---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /ru/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте некоторый текст и пометьте его сноской, у которой свойство IsAuto по умолчанию установлено в "true",
# чтобы маркер, видимый в основном тексте, был автоматически пронумерован как "1",
# и сноска появится внизу страницы.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Вставьте ещё текст и пометьте его конечной сноской с пользовательским маркером ссылки,
# который будет использоваться вместо числа "2" и установит "IsAuto" в false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Сноски всегда появляются внизу текста, к которому они относятся,
# поэтому разрыв страницы не повлияет на сноску.
# С другой стороны, конечные сноски всегда находятся в конце документа
# поэтому этот разрыв страницы переместит конечную сноску на следующую страницу.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

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

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

