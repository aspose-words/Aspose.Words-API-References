---
title: Footnote.footnote_type property
linktitle: footnote_type property
articleTitle: footnote_type property
second_title: Aspose.Words for Python
description: "Footnote.footnote_type property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /ru/python-net/aspose.words.notes/footnote/footnote_type/
---

## Footnote.footnote_type property

Returns a value that specifies whether this is a footnote or endnote.


```python
@property
def footnote_type(self) -> aspose.words.notes.FootnoteType:
    ...

```

### Examples

Shows the difference between footnotes and endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ниже представлены два способа присоединения нумерованных ссылок к тексту. Оба этих ссылки добавят a
# маленький надстрочный маркер ссылки в месте, где мы их вставляем.
# Маркер ссылки по умолчанию является индексным номером ссылки среди всех ссылок в документе.
# Каждая ссылка также создаст запись, которая будет иметь тот же маркер ссылки, что и в основном тексте.
# и текст ссылки, который мы передадим методу "InsertFootnote" построителя документа.
# 1 -  Сноска, запись которой появится на той же странице, что и текст, к которому она относится:
builder.write('Footnote referenced main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text, will appear at the bottom of the page that contains the referenced text.')
# 2 -  Концевая сноска, запись которой появится в конце документа:
builder.write('Endnote referenced main body text.')
endnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote text, will appear at the very end of the document.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.notes.FootnoteType.FOOTNOTE, footnote.footnote_type)
self.assertEqual(aw.notes.FootnoteType.ENDNOTE, endnote.footnote_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.FootnoteEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

