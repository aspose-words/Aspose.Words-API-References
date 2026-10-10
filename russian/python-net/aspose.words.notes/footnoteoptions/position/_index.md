---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /ru/python-net/aspose.words.notes/footnoteoptions/position/
---

## FootnoteOptions.position property

Specifies the footnotes position.


```python
@property
def position(self) -> aspose.words.notes.FootnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.FootnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Сноска — это способ добавить ссылку или боковой комментарий к тексту.
# которая не вмешивается в поток основного текста.
# Вставка сноски добавляет небольшой верхний индекс в виде символа ссылки.
# в основном тексте, где мы вставляем сноску.
# Каждая сноска также создает запись внизу страницы, состоящую из символа.
# который соответствует символу ссылки в основном тексте.
# Текст ссылки, который мы передаем методу "InsertFootnote" построителя документа.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# Мы можем использовать свойство "Position", чтобы определить, где документ разместит все свои сноски.
# Если мы установим значение свойства "Position" в "FootnotePosition.BottomOfPage",
# каждая сноска будет отображаться внизу страницы, содержащей её метку ссылки. Это значение по умолчанию.
# Если мы установим значение свойства "Position" в "FootnotePosition.BeneathText",
# каждая сноска будет отображаться в конце текста страницы, содержащего её метку ссылки.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

