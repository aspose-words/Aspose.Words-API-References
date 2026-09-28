---
title: DocSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/docsaveoptions/save_format/
---

## DocSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) or [SaveFormat.DOT](../../../aspose.words/saveformat/#DOT).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to set save options for older Microsoft Word formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
# حدد كلمة مرور ستحمي تحميل الوثيقة بواسطة Microsoft Word أو Aspose.Words.
# لاحظ أن هذا لا يشفر محتويات الوثيقة بأي شكل.
options.password = 'MyPassword'
# إذا كانت الوثيقة تحتوي على إيصال توجيه، يمكننا الحفاظ عليه أثناء الحفظ بتعيين هذه العلامة إلى true.
options.save_routing_slip = True
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', save_options=options)
# لكي نتمكن من تحميل الوثيقة،
# سنحتاج إلى تطبيق كلمة المرور التي حددناها في كائن DocSaveOptions داخل كائن LoadOptions.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc')
load_options = aw.loading.LoadOptions(password='MyPassword')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', load_options=load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

