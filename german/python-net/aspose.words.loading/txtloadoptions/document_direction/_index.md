---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /de/python-net/aspose.words.loading/txtloadoptions/document_direction/
---

## TxtLoadOptions.document_direction property

Gets or sets a document direction.
The default value is [DocumentDirection.LEFT_TO_RIGHT](../../documentdirection/#LEFT_TO_RIGHT).



```python
@property
def document_direction(self) -> aspose.words.loading.DocumentDirection:
    ...

@document_direction.setter
def document_direction(self, value: aspose.words.loading.DocumentDirection):
    ...

```

### Examples

Shows how to detect plaintext document text direction.

```python
# Erstellen Sie ein "TxtLoadOptions"‑Objekt, das wir an den Konstruktor eines Dokuments übergeben können
# um zu ändern, wie wir ein Klartextdokument laden.
load_options = aw.loading.TxtLoadOptions()
# Setzen Sie die Eigenschaft "DocumentDirection" auf "DocumentDirection.Auto", erkennt automatisch
# die Richtung jedes Textabsatzes, den Aspose.Words aus Klartext lädt.
# Die "Bidi"‑Eigenschaft jedes Absatzes speichert dessen Richtung.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Hebräischen Text als Rechts‑nach‑Links erkennen.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Englischen Text als Rechts‑nach‑Links erkennen.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

