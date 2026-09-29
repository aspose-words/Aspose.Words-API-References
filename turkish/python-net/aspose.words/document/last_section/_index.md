---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 250
url: /tr/python-net/aspose.words/document/last_section/
---

## Document.last_section property

Gets the last section in the document.


```python
@property
def last_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# Boş bir belge varsayılan olarak bir bölüm içerir,
# bu bölüm, düzenleyebileceğimiz alt düğümler içerir.
self.assertEqual(1, doc.sections.count)
# İlk bölüme metin eklemek için bir document builder kullanın.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Bir bölüm sonu ekleyerek ikinci bir bölüm oluşturun.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# Her bölümün kendi sayfa ayarları vardır.
# İkinci bölmedeki metni iki sütuna bölüştürebiliriz.
# Bu, ilk bölmedeki metni etkilemez.
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

