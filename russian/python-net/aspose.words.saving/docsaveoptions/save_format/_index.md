---
title: DocSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /ru/python-net/aspose.words.saving/docsaveoptions/save_format/
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

