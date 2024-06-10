---
title: DocSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /python-net/aspose.words.saving/docsaveoptions/save_format/
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
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
# Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
# Note that this does not encrypt the contents of the document in any way.
options.password = 'MyPassword'
# If the document contains a routing slip, we can preserve it while saving by setting this flag to True.
options.save_routing_slip = True
doc.save(ARTIFACTS_DIR + 'DocSaveOptions.save_as_doc.doc', options)
# To be able to load the document,
# we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
with self.assertRaises(Exception):
    doc = aw.Document(ARTIFACTS_DIR + 'DocSaveOptions.save_as_doc.doc')
load_options = aw.loading.LoadOptions('MyPassword')
doc = aw.Document(ARTIFACTS_DIR + 'DocSaveOptions.save_as_doc.doc', load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

