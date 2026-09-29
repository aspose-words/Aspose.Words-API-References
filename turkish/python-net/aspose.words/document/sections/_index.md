---
title: Document.sections property
linktitle: sections property
articleTitle: sections property
second_title: Aspose.Words for Python
description: "Document.sections property. Returns a collection that represents all sections in the document."
type: docs
weight: 400
url: /tr/python-net/aspose.words/document/sections/
---

## Document.sections property

Returns a collection that represents all sections in the document.


```python
@property
def sections(self) -> aspose.words.SectionCollection:
    ...

```

### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('This text is in section 1.')
# Bölüm sonu türleri, yeni bir bölümün önceki bölümden nasıl ayrıldığını belirler.
# Aşağıda beş tür bölüm sonu bulunmaktadır.
# 1 -  Sonraki bölümü yeni bir sayfada başlatır:
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('This text is in section 2.')
self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)
# 2 -  Sonraki bölümü mevcut sayfada başlatır:
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('This text is in section 3.')
self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)
# 3 -  Sonraki bölümü yeni çift sayfada başlatır:
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln('This text is in section 4.')
self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)
# 4 -  Sonraki bölümü yeni tek sayfada başlatır:
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln('This text is in section 5.')
self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)
# 5 -  Sonraki bölümü yeni bir sütunda başlatır:
columns = builder.page_setup.text_columns
columns.set_count(2)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln('This text is in section 6.')
self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetSectionStart.docx')
```

Shows how to add and remove sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
self.assertEqual('Section 1\x0cSection 2', doc.get_text().strip())
# Belgeden ilk bölümü silin.
doc.sections.remove_at(0)
self.assertEqual('Section 2', doc.get_text().strip())
# Şu anda ilk bölüm olan kopyayı belgenin sonuna ekleyin.
last_section_idx = doc.sections.count - 1
new_section = doc.sections[last_section_idx].clone()
doc.sections.add(new_section)
self.assertEqual('Section 2\x0cSection 2', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

