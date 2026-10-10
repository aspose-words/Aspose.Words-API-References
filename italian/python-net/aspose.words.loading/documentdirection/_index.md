---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /it/python-net/aspose.words.loading/documentdirection/
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
# Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
# per modificare il modo in cui carichiamo un documento di testo semplice.
load_options = aw.loading.TxtLoadOptions()
# Imposta la proprietà "DocumentDirection" su "DocumentDirection.Auto" per rilevare automaticamente
# la direzione di ogni paragrafo di testo che Aspose.Words carica dal testo semplice.
# La proprietà "Bidi" di ogni paragrafo memorizzerà la sua direzione.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Rileva il testo ebraico da destra a sinistra.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Rileva il testo inglese da destra a sinistra.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../)

