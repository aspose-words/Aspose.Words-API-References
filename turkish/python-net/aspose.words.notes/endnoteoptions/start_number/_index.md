---
title: EndnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "EndnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered endnotes."
type: docs
weight: 40
url: /tr/python-net/aspose.words.notes/endnoteoptions/start_number/
---

## EndnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered endnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [EndnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Dipnotlar ve sonnotlar, metne bir referans veya yan yorum eklemenin bir yoludur.
# bu, ana metin akışına müdahale etmez.
# Bir dipnot/sonnot eklemek, küçük bir üst simge referans işareti ekler.
# dipnotu/sonnotu eklediğimiz ana metin içinde.
# Her dipnot/sonnot ayrıca bir giriş oluşturur, bu giriş bir sembolden oluşur
# bu, ana metindeki referans sembolüyle eşleşir.
# Belge oluşturucusunun "InsertEndnote" metoduna geçtiğimiz referans metni.
# Dipnot girişleri, varsayılan olarak, içeren her sayfanın alt kısmında görünür
# referans sembollerini, ve sonnotlar belgenin sonunda görünür.
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
# Varsayılan olarak, her dipnot ve sonnot için referans sembolü onun indeksidir
# belgenin tüm dipnot/sonnotları arasında. Her belge ayrı sayımlar tutar
# dipnotlar ve sonnotlar için, ikisi de 1'den başlar.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Belgeyi ... elde etmek için "StartNumber" özelliğini kullanabiliriz
# dipnot veya sonnot sayımını farklı bir sayıdan başlatmak.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

