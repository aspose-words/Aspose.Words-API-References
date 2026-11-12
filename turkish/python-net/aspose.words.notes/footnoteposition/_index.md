---
title: FootnotePosition enumeration
linktitle: FootnotePosition enumeration
articleTitle: FootnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnotePosition enumeration. Defines the footnote position."
type: docs
weight: 60
url: /tr/python-net/aspose.words.notes/footnoteposition/
---

## FootnotePosition enumeration

Defines the footnote position.


### Members

| Name | Description |
| --- | --- |
| BOTTOM_OF_PAGE | Footnotes are output at the bottom of each page. |
| BENEATH_TEXT | Footnotes are output beneath text on each page. |

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir dipnot, metne bir referans veya yan yorum eklemenin bir yoludur.
# bu, ana metin akışına müdahale etmez.
# Bir dipnot eklemek, küçük bir üst simge referans işareti ekler.
# dipnotu eklediğimiz ana metin içinde.
# Her dipnot ayrıca sayfanın alt kısmında bir giriş oluşturur; bu giriş bir sembolden oluşur.
# bu, ana metindeki referans sembolüyle eşleşir.
# Belge oluşturucunun "InsertFootnote" yöntemine gönderdiğimiz referans metni.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# "Position" özelliğini kullanarak belgenin tüm dipnotları nereye yerleştireceğini belirleyebiliriz.
# "Position" özelliğinin değerini "FootnotePosition.BottomOfPage" olarak ayarlarsak,
# her dipnot, referans işaretini içeren sayfanın alt kısmında görünecektir. Bu, varsayılan değerdir.
# "Position" özelliğinin değerini "FootnotePosition.BeneathText" olarak ayarlarsak,
# her dipnot, referans işaretini içeren sayfanın metninin sonunda görünecektir.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)

