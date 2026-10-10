---
title: FieldRD.is_path_relative property
linktitle: is_path_relative property
articleTitle: is_path_relative property
second_title: Aspose.Words for Python
description: "FieldRD.is_path_relative property. Gets or sets whether the path is relative to the current document."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/fieldrd/is_path_relative/
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
# Используйте DocumentBuilder, чтобы вставить оглавление,
# а затем добавьте одну запись оглавления на следующей странице.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
builder.writeln('TOC entry from within this document')
# Вставьте поле RD, которое ссылается на другой документ локальной файловой системы в его свойстве FileName.
# Содержание теперь также будет принимать все заголовки из ссылочного документа в качестве записей для своей таблицы.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF_DOC, update_field=True).as_field_rd()
field.file_name = ARTIFACTS_DIR + 'ReferencedDocument.docx'
self.assertEqual(f' RD  {ARTIFACTS_DIR.replace(chr(92), chr(92) + chr(92))}ReferencedDocument.docx', field.get_field_code())
# Создайте документ, на который ссылается поле RD, и вставьте заголовок.
# Этот заголовок появится как запись в поле TOC в нашем первом документе.
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

