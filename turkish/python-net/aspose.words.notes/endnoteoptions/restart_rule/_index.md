---
title: EndnoteOptions.restart_rule property
linktitle: restart_rule property
articleTitle: restart_rule property
second_title: Aspose.Words for Python
description: "EndnoteOptions.restart_rule property. Determines when automatic numbering restarts."
type: docs
weight: 30
url: /tr/python-net/aspose.words.notes/endnoteoptions/restart_rule/
---

## EndnoteOptions.restart_rule property

Determines when automatic numbering restarts.


```python
@property
def restart_rule(self) -> aspose.words.notes.FootnoteNumberingRule:
    ...

@restart_rule.setter
def restart_rule(self, value: aspose.words.notes.FootnoteNumberingRule):
    ...

```

### Remarks

Not all values are applicable to endnotes.
To ascertain which values are applicable see [FootnoteNumberingRule](../../footnotenumberingrule/).




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

