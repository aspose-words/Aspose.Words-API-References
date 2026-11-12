---
title: FootnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "FootnoteOptions.number_style property. Specifies the number format for automatically numbered footnotes."
type: docs
weight: 20
url: /tr/python-net/aspose.words.notes/footnoteoptions/number_style/
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
# Dipnotlar ve sonnotlar, metne bir referans veya yan yorum eklemenin bir yoludur.
# bu, ana metin akışına müdahale etmez.
# Bir dipnot/sonnot eklemek, küçük bir üst simge referans işareti ekler.
# dipnotu/sonnotu eklediğimiz ana metin içinde.
# Her dipnot/sonnot ayrıca bir giriş oluşturur; bu giriş referansla eşleşen bir sembolden oluşur.
# ana metin içindeki sembol. Belge oluşturucunun "InsertEndnote" yöntemine gönderdiğimiz referans metni.
# Dipnot girişleri, varsayılan olarak, içeren her sayfanın alt kısmında görünür
# referans sembollerini, ve sonnotlar belgenin sonunda görünür.
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
# Varsayılan olarak, her dipnot ve sonnot için referans sembolü onun indeksidir
# belgenin tüm dipnot/sonnotları arasında. Her belge ayrı sayımlar tutar
# dipnotlar ve sonnotlar için. Varsayılan olarak, dipnotlar sayılarını Arap rakamlarıyla gösterir,
# ve sonnotlar sayılarını küçük harf Roma rakamlarıyla gösterir.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# "NumberStyle" özelliğini kullanarak dipnot ve sonnotlara özel numaralandırma stilleri uygulayabiliriz.
# Bu, özel referans işaretlerine sahip dipnot/sonnotları etkilemez.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

