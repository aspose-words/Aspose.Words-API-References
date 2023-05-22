---
title: DocSaveOptions constructor
linktitle: DocSaveOptions constructor
articleTitle: DocSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.DocSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/docsaveoptions/__init__/
---

## DocSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) format.



```python
def __init__(self):
    ...
```

## DocSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) or
[SaveFormat.DOT](../../../aspose.words/saveformat/#DOT) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to set save options for older Microsoft Word formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write("Hello world!")

options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)

# Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
# Note that this does not encrypt the contents of the document in any way.
options.password = "MyPassword"

# If the document contains a routing slip, we can preserve it while saving by setting this flag to True.
options.save_routing_slip = True

doc.save(ARTIFACTS_DIR + "DocSaveOptions.save_as_doc.doc", options)

# To be able to load the document,
# we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
with self.assertRaises(Exception):
    doc = aw.Document(ARTIFACTS_DIR + "DocSaveOptions.save_as_doc.doc")

load_options = aw.loading.LoadOptions("MyPassword")
doc = aw.Document(ARTIFACTS_DIR + "DocSaveOptions.save_as_doc.doc", load_options)

self.assertEqual("Hello world!", doc.get_text().strip())
```

## See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

