---
title: EndnotePosition enumeration
linktitle: EndnotePosition enumeration
articleTitle: EndnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.EndnotePosition enumeration. Defines the endnote position."
type: docs
weight: 20
url: /tr/python-net/aspose.words.notes/endnoteposition/
---

## EndnotePosition enumeration

Defines the endnote position.


### Members

| Name | Description |
| --- | --- |
| END_OF_SECTION | Endnotes are output at the end of the section. |
| END_OF_DOCUMENT | Endnotes are output at the end of the document. |

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir dipnot, metne bir referans veya yan yorum eklemenin bir yoludur
# bu, ana metin akışına müdahale etmez.
# Bir dipnot eklemek, küçük bir üst simge referans işareti ekler
# dipnotu eklediğimiz ana metin içinde.
# Her dipnot ayrıca belgenin sonunda bir sembolden oluşan bir giriş oluşturur
# bu, ana metindeki referans sembolüyle eşleşir.
# Belge oluşturucusunun "InsertEndnote" metoduna geçtiğimiz referans metni.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# "Position" özelliğini, belgenin tüm dipnotlarını nereye yerleştireceğini belirlemek için kullanabiliriz.
# "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
# her dipnot, belgenin sonunda bir koleksiyonda görünecek. Bu varsayılan değerdir.
# "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
# her dipnot, dipnotun referans işaretini içeren metnin bulunduğu bölümün sonunda bir koleksiyonda görünecektir.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [EndnoteOptions](../endnoteoptions/)

