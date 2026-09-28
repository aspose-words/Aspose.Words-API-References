---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /de/python-net/aspose.words.loading/documentdirection/
---

## DocumentDirection enumeration

Allows to specify the direction to flow the text in a document.


### Members

| Name | Description |
| --- | --- |
| LEFT_TO_RIGHT | Left to right direction. |
| RIGHT_TO_LEFT | Right to left direction. |
| AUTO | Auto-detect direction. |

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

* module [aspose.words.loading](../)

