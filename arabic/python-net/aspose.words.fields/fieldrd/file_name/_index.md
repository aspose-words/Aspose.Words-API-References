---
title: FieldRD.file_name property
linktitle: file_name property
articleTitle: file_name property
second_title: Aspose.Words for Python
description: "FieldRD.file_name property. Gets or sets the name of the file to include when generating a table of contents, table of authorities, or index."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldrd/file_name/
---

## FieldRD.file_name property

Gets or sets the name of the file to include when generating a table of contents, table of authorities, or index.


```python
@property
def file_name(self) -> str:
    ...

@file_name.setter
def file_name(self, value: str):
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
# استخدم منشئ المستند لإدراج جدول محتويات،
# ثم أضف مدخلًا واحدًا لجدول المحتويات في الصفحة التالية.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
builder.writeln('TOC entry from within this document')
# أدرج حقل RD، الذي يشير إلى مستند نظام ملفات محلي آخر في خاصية FileName الخاصة به.
# ستقبل TOC الآن أيضًا جميع العناوين من المستند المشار إليه كمدخلات لجدوله.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF_DOC, update_field=True).as_field_rd()
field.file_name = ARTIFACTS_DIR + 'ReferencedDocument.docx'
self.assertEqual(f' RD  {ARTIFACTS_DIR.replace(chr(92), chr(92) + chr(92))}ReferencedDocument.docx', field.get_field_code())
# أنشئ المستند الذي يشير إليه حقل RD وأدرج عنوانًا.
# سيظهر هذا العنوان كمدخل في حقل TOC في مستندنا الأول.
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

