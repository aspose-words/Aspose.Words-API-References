---
title: DocSaveOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "DocSaveOptions.password property. Gets/sets a password to encrypt document using RC4 encryption method."
type: docs
weight: 40
url: /ar/python-net/aspose.words.saving/docsaveoptions/password/
---

## DocSaveOptions.password property

Gets/sets a password to encrypt document using RC4 encryption method.


```python
@property
def password(self) -> str:
    ...

@password.setter
def password(self, value: str):
    ...

```

### Remarks

In order to save document without encryption this property should be ``None`` or empty string.




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

