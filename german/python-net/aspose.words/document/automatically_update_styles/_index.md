---
title: Document.automatically_update_styles property
linktitle: automatically_update_styles property
articleTitle: automatically_update_styles property
second_title: Aspose.Words for Python
description: "Document.automatically_update_styles property. Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word."
type: docs
weight: 30
url: /de/python-net/aspose.words/document/automatically_update_styles/
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
# Microsoft‑Word‑Dokumente enthalten standardmäßig eine angehängte Vorlage mit dem Namen "Normal.dotm".
# Für leere Aspose.Words‑Dokumente gibt es keine Standardvorlage.
self.assertEqual('', doc.attached_template)
# Eine Vorlage anhängen, dann das Flag setzen, um Stiländerungen anzuwenden
# innerhalb der Vorlage auf Stile in unserem Dokument.
doc.attached_template = MY_DIR + 'Business brochure.dotx'
doc.automatically_update_styles = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.AutomaticallyUpdateStyles.docx')
```

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Automatisches Aktualisieren von Stilen aktivieren, aber kein Vorlagendokument anhängen.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Da es kein Vorlagendokument gibt, hatte das Dokument keinen Ort, um Stiländerungen zu verfolgen.
# Verwenden Sie ein SaveOptions‑Objekt, um automatisch eine Vorlage festzulegen
# falls ein Dokument, das wir speichern, keine hat.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

