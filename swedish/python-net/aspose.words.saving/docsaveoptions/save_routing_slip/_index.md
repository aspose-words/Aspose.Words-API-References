---
title: DocSaveOptions.save_routing_slip property
linktitle: save_routing_slip property
articleTitle: save_routing_slip property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_routing_slip property. When ``False``, RoutingSlip data is not saved to output document"
type: docs
weight: 70
url: /sv/python-net/aspose.words.saving/docsaveoptions/save_routing_slip/
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

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

