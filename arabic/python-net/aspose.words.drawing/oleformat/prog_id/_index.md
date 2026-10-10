---
title: OleFormat.prog_id property
linktitle: prog_id property
articleTitle: prog_id property
second_title: Aspose.Words for Python
description: "OleFormat.prog_id property. Gets or sets the ProgID of the OLE object."
type: docs
weight: 90
url: /ar/python-net/aspose.words.drawing/oleformat/prog_id/
---

## OleFormat.prog_id property

Gets or sets the ProgID of the OLE object.


```python
@property
def prog_id(self) -> str:
    ...

@prog_id.setter
def prog_id(self, value: str):
    ...

```

### Remarks

The ProgID property is not always present in Microsoft Word documents and cannot be relied upon.

Cannot be ``None``.

The default value is an empty string.




### Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(file_name=MY_DIR + 'OLE spreadsheet.docm')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
# كائن OLE في الشكل الأول هو جدول بيانات Microsoft Excel.
ole_format = shape.ole_format
self.assertEqual('Excel.Sheet.12', ole_format.prog_id)
# كائننا ليس محدثًا تلقائيًا ولا مقفلًا من التحديثات.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)
# إذا كنا نخطط لحفظ كائن OLE في ملف على نظام الملفات المحلي،
# يمكننا استخدام الخاصية "SuggestedExtension" لتحديد امتداد الملف الذي يجب تطبيقه على الملف.
self.assertEqual('.xlsx', ole_format.suggested_extension)
# فيما يلي طريقتان لحفظ كائن OLE في ملف على نظام الملفات المحلي.
# 1 -  احفظه عبر تدفق:
with system_helper.io.FileStream(ARTIFACTS_DIR + 'OLE spreadsheet extracted via stream' + ole_format.suggested_extension, system_helper.io.FileMode.CREATE) as fs:
    ole_format.save(stream=fs)
# 2 -  احفظه مباشرةً إلى اسم ملف:
ole_format.save(file_name=ARTIFACTS_DIR + 'OLE spreadsheet saved directly' + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../../)
* class [OleFormat](../)

