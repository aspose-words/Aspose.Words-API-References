---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /sv/python-net/aspose.words.loading/txtloadoptions/document_direction/
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

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

