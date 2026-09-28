---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /fr/python-net/aspose.words/document/automatically_update_styles/
---

## Document.automatically_update_styles property

Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the
attached template each time the document is opened in MS Word.


```python
@property
def automatically_update_styles(self) -> bool:
    ...

@automatically_update_styles.setter
def automatically_update_styles(self, value: bool):
    ...

```

### Examples

Shows how to attach a template to a document.

```python
doc = aw.Document()
# Les documents Microsoft Word sont fournis par défaut avec un modèle joint appelé "Normal.dotm".
# Il n'existe aucun modèle par défaut pour les documents Aspose.Words vierges.
self.assertEqual('', doc.attached_template)
# Attachez un modèle, puis définissez le drapeau pour appliquer les modifications de style
# dans le modèle aux styles de notre document.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Activez la mise à jour automatique des styles, mais n'attachez pas de document modèle.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Comme il n'y a pas de document modèle, le document n'avait nulle part où suivre les modifications de style.
# Utilisez un objet SaveOptions pour définir automatiquement un modèle
# si le document que nous enregistrons n'en possède pas.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

