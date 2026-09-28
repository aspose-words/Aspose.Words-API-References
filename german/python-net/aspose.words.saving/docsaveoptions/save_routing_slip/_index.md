---
title: DocSaveOptions.save_routing_slip property
linktitle: save_routing_slip property
articleTitle: save_routing_slip property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_routing_slip property. When ``False``, RoutingSlip data is not saved to output document"
type: docs
weight: 70
url: /de/python-net/aspose.words.saving/docsaveoptions/save_routing_slip/
---

## DocSaveOptions.save_routing_slip property

When ``False``, RoutingSlip data is not saved to output document.
Default value is ``True``.



```python
@property
def save_routing_slip(self) -> bool:
    ...

@save_routing_slip.setter
def save_routing_slip(self, value: bool):
    ...

```

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

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

