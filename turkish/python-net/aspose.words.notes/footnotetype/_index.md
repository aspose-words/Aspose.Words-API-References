---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /tr/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Biraz metin ekleyin ve varsayılan olarak "true" ayarlı IsAuto özelliğine sahip bir dipnotla işaretleyin,
# böylece gövde metninde görülen işaretçi "1" olarak otomatik numaralandırılacak,
# ve dipnot sayfanın alt kısmında görünecek.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Daha fazla metin ekleyin ve özel bir referans işaretiyle bir sonnotla işaretleyin,
# bu, "2" numarası yerine kullanılacak ve "IsAuto" özelliğini false olarak ayarlayacak.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Dipnotlar her zaman referans verilen metnin altında görünür,
# bu yüzden bu sayfa sonu dipnota etki etmeyecek.
# Öte yandan, sonnotlar her zaman belgenin sonunda bulunur
# bu yüzden bu sayfa sonu sonnotu bir sonraki sayfaya itecektir.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Metin ekleyin ve bir dipnotla referans verin. Bu dipnot küçük bir üst simge referansı yerleştirecek
# referans verdiği metnin ardından bir işaret koyacak ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturacak.
# Bu giriş dipnotun referans işaretini ve referans metnini içerecek,
# ki bunu belge oluşturucunun "InsertFootnote" metoduna geçireceğiz.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Bu özellik "true" olarak ayarlanırsa, dipnotumuzun referans işareti
# bölümdeki tüm dipnotlar arasında indeks olacaktır.
# Bu ilk dipnot, bu yüzden referans işareti "1" olacaktır.
self.assertTrue(footnote.is_auto)
# Dipnotun içindeki referans metnini düzenlemek için belge oluşturucuyu dipnota taşıyabiliriz.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti ayarlayabiliriz.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# "IsAuto" bayrağı true olarak ayarlanmış bir yer imi hâlâ gerçek indeksini gösterecek
# önceki yer imleri özel referans işaretleri gösterse bile, bu yer iminin referans işareti "3" olacaktır.
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

