---
title: FootnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "FootnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered footnotes."
type: docs
weight: 50
url: /ru/python-net/aspose.words.notes/footnoteoptions/start_number/
---

## FootnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered footnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [FootnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Сноски и концевые сноски — это способ добавить ссылку или боковой комментарий к тексту.
# которая не вмешивается в поток основного текста.
# Вставка сноски/концевой сноски добавляет небольшой верхний индекс в виде символа ссылки.
# в основном тексте, где мы вставляем сноску/концевую сноску.
# Каждая сноска/конечная сноска также создаёт запись, состоящую из символа
# который соответствует символу ссылки в основном тексте.
# Текст ссылки, который мы передаём методу "InsertEndnote" построителя документа.
# Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
# их символы ссылок, а концевые сноски отображаются в конце документа.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# По умолчанию символ ссылки для каждой сноски и концевой сноски — её индекс
# среди всех сносок/концевых сносок документа. Каждый документ ведёт отдельный счёт
# для сносок и конечных сносок, которые обе начинаются с 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Мы можем использовать свойство "StartNumber", чтобы документ
# начал счётчик сноски или конечной сноски с другого числа.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

