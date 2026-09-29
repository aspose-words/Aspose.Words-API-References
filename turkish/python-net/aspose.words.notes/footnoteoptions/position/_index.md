---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /tr/python-net/aspose.words.notes/footnoteoptions/position/
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

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

