---
title: EndnoteOptions class
linktitle: EndnoteOptions class
articleTitle: EndnoteOptions class
second_title: Aspose.Words for Python
description: "aspose.words.notes.EndnoteOptions class. Represents the endnote numbering options for a document or section"
type: docs
weight: 10
url: /ru/python-net/aspose.words.notes/endnoteoptions/
---

## EndnoteOptions class

Represents the endnote numbering options for a document or section.
To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/python-net/working-with-footnote-and-endnote/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [number_style](./number_style/) | Specifies the number format for automatically numbered endnotes. |
| [position](./position/) | Specifies the endnotes position. |
| [restart_rule](./restart_rule/) | Determines when automatic numbering restarts. |
| [start_number](./start_number/) | Specifies the starting number or character for the first automatically numbered endnotes. |

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Концевая сноска — это способ добавить ссылку или боковой комментарий к тексту
# которая не вмешивается в поток основного текста.
# Вставка концевой сноски добавляет небольшой верхний индексный символ ссылки
# в основном тексте там, где мы вставляем сноску.
# Каждая концевая сноска также создаёт запись в конце документа, состоящую из символа
# который соответствует символу ссылки в основном тексте.
# Текст ссылки, который мы передаём методу "InsertEndnote" построителя документа.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Мы можем использовать свойство "Position", чтобы определить, где документ разместит все свои концевые сноски.
# Если установить значение свойства "Position" в "EndnotePosition.EndOfDocument",
# каждая сноска появится в коллекции в конце документа. Это значение по умолчанию.
# Если установить значение свойства "Position" в "EndnotePosition.EndOfSection",
# каждая сноска будет отображаться в коллекции в конце раздела, текст которого содержит метку ссылки сноски.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

Shows how to change the number style of footnote/endnote reference marks.

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
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# По умолчанию символ ссылки для каждой сноски и концевой сноски — её индекс
# среди всех сносок/концевых сносок документа. Каждый документ ведёт отдельный счёт
# для сносок и для концевых сносок. По умолчанию сноски отображают свои номера арабскими цифрами,
# а концевые сноски отображают свои номера римскими цифрами в нижнем регистре.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# Мы можем использовать свойство "NumberStyle", чтобы применить пользовательские стили нумерации к сноскам и концевым сноскам.
# Это не повлияет на сноски/концевые сноски с пользовательскими метками ссылок.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

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

* module [aspose.words.notes](../)
* property [Document.endnote_options](../../aspose.words/document/endnote_options/)
* property [PageSetup.endnote_options](../../aspose.words/pagesetup/endnote_options/)

