---
title: FootnoteOptions.restart_rule property
linktitle: restart_rule property
articleTitle: restart_rule property
second_title: Aspose.Words for Python
description: "FootnoteOptions.restart_rule property. Determines when automatic numbering restarts."
type: docs
weight: 40
url: /ru/python-net/aspose.words.notes/footnoteoptions/restart_rule/
---

## FootnoteOptions.restart_rule property

Determines when automatic numbering restarts.


```python
@property
def restart_rule(self) -> aspose.words.notes.FootnoteNumberingRule:
    ...

@restart_rule.setter
def restart_rule(self, value: aspose.words.notes.FootnoteNumberingRule):
    ...

```

### Examples

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Сноски и концевые сноски — это способ добавить ссылку или боковой комментарий к тексту.
# которая не вмешивается в поток основного текста.
# Вставка сноски/концевой сноски добавляет небольшой верхний индекс в виде символа ссылки.
# в основном тексте, где мы вставляем сноску/концевую сноску.
# Каждая сноска/концевая сноска также создает запись, состоящую из символа, соответствующего ссылке
# символ в основном тексте. Текст ссылки, который мы передаем методу "InsertEndnote" построителя документа.
# Записи сносок по умолчанию отображаются внизу каждой страницы, содержащей
# их символы ссылок, а концевые сноски отображаются в конце документа.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# По умолчанию символ ссылки для каждой сноски и концевой сноски — её индекс
# среди всех сносок/концевых сносок документа. Каждый документ ведёт отдельный счёт
# для сносок и концевых сносок и не сбрасывает эти счётчики ни в какой момент.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Мы можем использовать свойство "RestartRule", чтобы документ перезапустился
# счётчики сносок/конечных сносок начинаются на новой странице или в разделе.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

