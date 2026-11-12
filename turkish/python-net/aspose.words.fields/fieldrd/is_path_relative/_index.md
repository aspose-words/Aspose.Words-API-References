---
title: FieldRD.is_path_relative property
linktitle: is_path_relative property
articleTitle: is_path_relative property
second_title: Aspose.Words for Python
description: "FieldRD.is_path_relative property. Gets or sets whether the path is relative to the current document."
type: docs
weight: 30
url: /tr/python-net/aspose.words.fields/fieldrd/is_path_relative/
---

## FieldRD.is_path_relative property

Gets or sets whether the path is relative to the current document.


```python
@property
def is_path_relative(self) -> bool:
    ...

@is_path_relative.setter
def is_path_relative(self, value: bool):
    ...

```

### Examples

Shows to use the RD field to create a table of contents entries from headings in other documents.

```python
import aspose.words as aw
import test_util
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir belge oluşturucu kullanarak bir içerik tablosu ekleyin,
# ve ardından sonraki sayfada içerik tablosu için bir giriş ekleyin.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
builder.writeln('TOC entry from within this document')
# FileName özelliğinde başka bir yerel dosya sistemi belgesine referans veren bir RD alanı ekleyin.
# TOC artık referans alınan belgeden tüm başlıkları tablosu için giriş olarak kabul edecek.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF_DOC, update_field=True).as_field_rd()
field.file_name = ARTIFACTS_DIR + 'ReferencedDocument.docx'
self.assertEqual(f' RD  {ARTIFACTS_DIR.replace(chr(92), chr(92) + chr(92))}ReferencedDocument.docx', field.get_field_code())
# RD alanının başvurduğu belgeyi oluşturun ve bir başlık ekleyin.
# Bu başlık, ilk belgemizdeki TOC alanında bir giriş olarak görünecek.
referenced_doc = aw.Document()
ref_doc_builder = aw.DocumentBuilder(doc=referenced_doc)
ref_doc_builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
ref_doc_builder.writeln('TOC entry from referenced document')
referenced_doc.save(file_name=ARTIFACTS_DIR + 'ReferencedDocument.docx')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.RD.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRD](../)

