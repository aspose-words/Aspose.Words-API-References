---
title: OlePackage.file_name property
linktitle: file_name property
articleTitle: file_name property
second_title: Aspose.Words for Python
description: "OlePackage.file_name property. Gets or sets OLE Package file name."
type: docs
weight: 20
url: /ar/python-net/aspose.words.drawing/olepackage/file_name/
---

## OlePackage.file_name property

Gets or sets OLE Package file name.


```python
@property
def file_name(self) -> str:
    ...

@file_name.setter
def file_name(self, value: str):
    ...

```

### Examples

Shows how insert an OLE object into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# تسمح كائنات OLE لنا بفتح ملفات أخرى في نظام الملفات المحلي باستخدام تطبيق مثبت آخر
# في نظام التشغيل لدينا عن طريق النقر المزدوج على الشكل الذي يحتوي على كائن OLE في جسم المستند.
# في هذه الحالة، سيكون ملفنا الخارجي أرشيف ZIP.
zip_file_bytes = system_helper.io.File.read_all_bytes(DATABASE_DIR + 'cat001.zip')
with io.BytesIO(zip_file_bytes) as stream:
    shape = builder.insert_ole_object(stream=stream, prog_id='Package', as_icon=True, presentation=None)
    shape.ole_format.ole_package.file_name = 'Package file name.zip'
    shape.ole_format.ole_package.display_name = 'Package display name.zip'
doc.save(file_name=ARTIFACTS_DIR + 'Shape.InsertOlePackage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [OlePackage](../)

