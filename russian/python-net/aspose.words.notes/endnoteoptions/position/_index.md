---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /ru/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

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

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

