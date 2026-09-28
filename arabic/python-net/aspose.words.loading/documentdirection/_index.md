---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /ar/python-net/aspose.words.loading/documentdirection/
---

## DocumentDirection enumeration

Allows to specify the direction to flow the text in a document.


### Members

| Name | Description |
| --- | --- |
| LEFT_TO_RIGHT | Left to right direction. |
| RIGHT_TO_LEFT | Right to left direction. |
| AUTO | Auto-detect direction. |

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

* module [aspose.words.loading](../)

