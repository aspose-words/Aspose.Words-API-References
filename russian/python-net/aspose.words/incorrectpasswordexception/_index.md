---
title: IncorrectPasswordException class
linktitle: IncorrectPasswordException class
articleTitle: IncorrectPasswordException class
second_title: Aspose.Words for Python
description: "aspose.words.IncorrectPasswordException class. Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing"
type: docs
weight: 660
url: /ru/python-net/aspose.words/incorrectpasswordexception/
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
# Установите пароль, который защитит загрузку документа в Microsoft Word или Aspose.Words.
# Обратите внимание, что это никоим образом не шифрует содержимое документа.
options.password = 'MyPassword'
# Если документ содержит маршрутный лист, мы можем сохранить его при сохранении, установив этот флаг в true.
options.save_routing_slip = True
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', save_options=options)
# Чтобы иметь возможность загрузить документ,
# нам потребуется применить пароль, указанный в объекте DocSaveOptions, в объекте LoadOptions.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc')
load_options = aw.loading.LoadOptions(password='MyPassword')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', load_options=load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

