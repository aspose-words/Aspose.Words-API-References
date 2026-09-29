---
title: DocSaveOptions constructor
linktitle: DocSaveOptions constructor
articleTitle: DocSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.DocSaveOptions constructor"
type: docs
weight: 10
url: /sv/python-net/aspose.words.saving/docsaveoptions/__init__/
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
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Can be [SaveFormat.DOC](../../../aspose.words/saveformat/#DOC) or [SaveFormat.DOT](../../../aspose.words/saveformat/#DOT). |

## Examples

Shows how to set save options for older Microsoft Word formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
# Ange ett lösenord som skyddar inläsningen av dokumentet i Microsoft Word eller Aspose.Words.
# Observera att detta inte krypterar dokumentets innehåll på något sätt.
options.password = 'MyPassword'
# Om dokumentet innehåller ett routningsblad kan vi bevara det vid sparning genom att sätta denna flagga till true.
options.save_routing_slip = True
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', save_options=options)
# För att kunna läsa in dokumentet,
# måste vi tillämpa lösenordet som vi specificerade i DocSaveOptions‑objektet i ett LoadOptions‑objekt.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc')
load_options = aw.loading.LoadOptions(password='MyPassword')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'DocSaveOptions.SaveAsDoc.doc', load_options=load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

## See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

