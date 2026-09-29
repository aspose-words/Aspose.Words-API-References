---
title: Footnote.reference_mark property
linktitle: reference_mark property
articleTitle: reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.reference_mark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /ru/python-net/aspose.words.notes/footnote/reference_mark/
---

## Footnote.reference_mark property

Gets/sets custom reference mark to be used for this footnote.
Default value is **empty string** (), meaning auto-numbered footnotes are used.



```python
@property
def reference_mark(self) -> str:
    ...

@reference_mark.setter
def reference_mark(self, value: str):
    ...

```

### Remarks

If this property is set to **empty string** () or ``None``, then [Footnote.is_auto](../is_auto/) property will automatically be set to ``True``, 
if set to anything else then [Footnote.is_auto](../is_auto/) will be set to ``False``.


RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.




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

