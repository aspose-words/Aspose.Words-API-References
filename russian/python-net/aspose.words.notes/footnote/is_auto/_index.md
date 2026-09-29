---
title: Footnote.is_auto property
linktitle: is_auto property
articleTitle: is_auto property
second_title: Aspose.Words for Python
description: "Footnote.is_auto property. Holds a value that specifies whether this is a auto-numbered footnote or  footnote with user defined custom reference mark."
type: docs
weight: 40
url: /ru/python-net/aspose.words.notes/footnote/is_auto/
---

## Footnote.is_auto property

Holds a value that specifies whether this is a auto-numbered footnote or 
footnote with user defined custom reference mark.


```python
@property
def is_auto(self) -> bool:
    ...

@is_auto.setter
def is_auto(self, value: bool):
    ...

```

### Remarks

[Footnote.reference_mark](../reference_mark/) initialized with empty string if [Footnote.is_auto](./) set to ``False``.



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

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

