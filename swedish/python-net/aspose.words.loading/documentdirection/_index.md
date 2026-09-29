---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /sv/python-net/aspose.words.loading/documentdirection/
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
# Skapa ett "TxtLoadOptions"‑objekt, som vi kan skicka till ett dokuments konstruktor
# för att ändra hur vi laddar ett klartext‑dokument.
load_options = aw.loading.TxtLoadOptions()
# Ställ in egenskapen "DocumentDirection" till "DocumentDirection.Auto" som automatiskt upptäcker
# riktningen för varje textparagraf som Aspose.Words laddar från klartext.
# Varje paragrafens "Bidi"‑egenskap kommer att lagra dess riktning.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Detektera hebreisk text som höger‑till‑vänster.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Detektera engelsk text som höger‑till‑vänster.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../)

