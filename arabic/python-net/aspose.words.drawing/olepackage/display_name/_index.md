---
title: OlePackage.display_name property
linktitle: display_name property
articleTitle: display_name property
second_title: Aspose.Words for Python
description: "OlePackage.display_name property. Gets or sets OLE Package display name."
type: docs
weight: 10
url: /ar/python-net/aspose.words.drawing/olepackage/display_name/
---

## OlePackage.display_name property

Gets or sets OLE Package display name.


```python
@property
def display_name(self) -> str:
    ...

@display_name.setter
def display_name(self, value: str):
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

