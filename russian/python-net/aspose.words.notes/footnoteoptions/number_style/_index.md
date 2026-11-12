---
title: FootnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "FootnoteOptions.number_style property. Specifies the number format for automatically numbered footnotes."
type: docs
weight: 20
url: /ru/python-net/aspose.words.notes/footnoteoptions/number_style/
---

## FootnoteOptions.number_style property

Specifies the number format for automatically numbered footnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

