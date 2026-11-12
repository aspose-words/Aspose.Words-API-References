---
title: Document.footnote_options property
linktitle: footnote_options property
articleTitle: footnote_options property
second_title: Aspose.Words for Python
description: "Document.footnote_options property. Provides options that control numbering and positioning of footnotes in this document."
type: docs
weight: 160
url: /tr/python-net/aspose.words/document/footnote_options/
---

## Document.footnote_options property

Provides options that control numbering and positioning of footnotes in this document.


```python
@property
def footnote_options(self) -> aspose.words.notes.FootnoteOptions:
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

Shows how to restart footnote/endnote numbering at certain places in the document.

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
# Varsayılan olarak, her dipnot ve sonnot için referans sembolü onun indeksidir
# belgenin tüm dipnot/sonnotları arasında. Her belge ayrı sayımlar tutar
# dipnotlar ve sonnotlar için geçerlidir ve bu sayımları hiçbir noktada yeniden başlatmaz.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Belgeyi yeniden başlatmak için "RestartRule" özelliğini kullanabiliriz
# dipnot/sonnot sayımları yeni bir sayfada veya bölümde başlar.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

