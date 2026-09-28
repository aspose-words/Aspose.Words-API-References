---
title: IncorrectPasswordException class
linktitle: IncorrectPasswordException class
articleTitle: IncorrectPasswordException class
second_title: Aspose.Words for Python
description: "aspose.words.IncorrectPasswordException class. Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing"
type: docs
weight: 660
url: /de/python-net/aspose.words/incorrectpasswordexception/
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
# Legen Sie ein Passwort fest, das das Laden des Dokuments durch Microsoft Word oder Aspose.Words schützt.
# Beachten Sie, dass dies den Inhalt des Dokuments in keiner Weise verschlüsselt.
options.password = 'MyPassword'
# Wenn das Dokument einen Routing Slip enthält, können wir ihn beim Speichern erhalten, indem wir dieses Flag auf true setzen.
options.save_routing_slip = True
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', save_options=options)
# Um das Dokument laden zu können,
# müssen wir das Passwort, das wir im DocSaveOptions-Objekt angegeben haben, in einem LoadOptions-Objekt anwenden.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc')
load_options = aw.loading.LoadOptions(password='MyPassword')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', load_options=load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

