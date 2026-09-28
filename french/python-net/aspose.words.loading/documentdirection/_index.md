---
title: DocumentDirection enumeration
linktitle: DocumentDirection enumeration
articleTitle: DocumentDirection enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentDirection enumeration. Allows to specify the direction to flow the text in a document."
type: docs
weight: 30
url: /fr/python-net/aspose.words.loading/documentdirection/
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
# Créez un objet "TxtLoadOptions", que nous pouvons transmettre au constructeur d'un document
# pour modifier la façon dont nous chargeons un document texte brut.
load_options = aw.loading.TxtLoadOptions()
# Définissez la propriété "DocumentDirection" sur "DocumentDirection.Auto" détecte automatiquement
# la direction de chaque paragraphe de texte que Aspose.Words charge depuis le texte brut.
# La propriété "Bidi" de chaque paragraphe stockera sa direction.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Détectez le texte hébreu comme de droite à gauche.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Détectez le texte anglais comme de droite à gauche.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words.loading](../)

