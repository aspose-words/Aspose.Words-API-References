---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /ar/python-net/aspose.words.loading/txtloadoptions/document_direction/
---

## TxtLoadOptions.document_direction property

Gets or sets a document direction.
The default value is [DocumentDirection.LEFT_TO_RIGHT](../../documentdirection/#LEFT_TO_RIGHT).



```python
@property
def document_direction(self) -> aspose.words.loading.DocumentDirection:
    ...

@document_direction.setter
def document_direction(self, value: aspose.words.loading.DocumentDirection):
    ...

```

### Examples

Shows how to detect plaintext document text direction.

```python
# أنشئ كائن "TxtLoadOptions"، الذي يمكننا تمريره إلى مُنشئ المستند
# لتعديل طريقة تحميل مستند نص عادي.
load_options = aw.loading.TxtLoadOptions()
# قم بتعيين خاصية "DocumentDirection" إلى "DocumentDirection.Auto" لتكتشف تلقائيًا
# اتجاه كل فقرة نصية تقوم Aspose.Words بتحميلها من النص العادي.
# ستخزن خاصية "Bidi" لكل فقرة اتجاهها.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# اكتشف النص العبري من اليمين إلى اليسار.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# اكتشف النص الإنجليزي من اليمين إلى اليسار.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

