---
title: IncorrectPasswordException class
linktitle: IncorrectPasswordException class
articleTitle: IncorrectPasswordException class
second_title: Aspose.Words for Python
description: "aspose.words.IncorrectPasswordException class. Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing"
type: docs
weight: 660
url: /ar/python-net/aspose.words/incorrectpasswordexception/
---

## IncorrectPasswordException class

Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




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

* module [aspose.words](../)

