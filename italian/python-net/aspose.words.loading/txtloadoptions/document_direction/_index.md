---
title: TxtLoadOptions.document_direction property
linktitle: document_direction property
articleTitle: document_direction property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.document_direction property. Gets or sets a document direction"
type: docs
weight: 50
url: /it/python-net/aspose.words.loading/txtloadoptions/document_direction/
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

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

