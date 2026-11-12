---
title: DocSaveOptions.save_routing_slip property
linktitle: save_routing_slip property
articleTitle: save_routing_slip property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_routing_slip property. When ``False``, RoutingSlip data is not saved to output document"
type: docs
weight: 70
url: /ru/python-net/aspose.words.saving/docsaveoptions/save_routing_slip/
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

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

