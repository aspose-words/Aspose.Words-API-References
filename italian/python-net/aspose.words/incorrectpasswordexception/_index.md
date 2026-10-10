---
title: IncorrectPasswordException class
linktitle: IncorrectPasswordException class
articleTitle: IncorrectPasswordException class
second_title: Aspose.Words for Python
description: "aspose.words.IncorrectPasswordException class. Thrown if a document is encrypted with a password and the password specified when opening the document is incorrect or missing"
type: docs
weight: 660
url: /it/python-net/aspose.words/incorrectpasswordexception/
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
# Imposta una password che proteggerà il caricamento del documento da parte di Microsoft Word o Aspose.Words.
# Nota che questo non crittografa in alcun modo il contenuto del documento.
options.password = 'MyPassword'
# Se il documento contiene un foglio di instradamento, possiamo preservarlo durante il salvataggio impostando questo flag su true.
options.save_routing_slip = True
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', save_options=options)
# Per poter caricare il documento,
# dovremo applicare la password che abbiamo specificato nell'oggetto DocSaveOptions in un oggetto LoadOptions.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc')
load_options = aw.loading.LoadOptions(password='MyPassword')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', load_options=load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

