---
title: Document.attached_template property
linktitle: attached_template property
articleTitle: attached_template property
second_title: Aspose.Words for Python
description: "Document.attached_template property. Gets or sets the full path of the template attached to the document."
type: docs
weight: 20
url: /it/python-net/aspose.words/document/attached_template/
---

## Document.attached_template property

Gets or sets the full path of the template attached to the document.


```python
@property
def attached_template(self) -> str:
    ...

@attached_template.setter
def attached_template(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws if you attempt to set to a ``None`` value. |

### Remarks

Empty string means the document is attached to the Normal template.




### Examples

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Abilita l'aggiornamento automatico degli stili, ma non allegare un documento modello.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Poiché non esiste un documento modello, il documento non aveva alcun luogo dove tenere traccia delle modifiche di stile.
# Usa un oggetto SaveOptions per impostare automaticamente un modello
# se un documento che stiamo salvando non ne ha uno.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* property [BuiltInDocumentProperties.template](../../../aspose.words.properties/builtindocumentproperties/template/)

