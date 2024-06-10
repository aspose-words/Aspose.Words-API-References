---
title: Document.attached_template property
linktitle: attached_template property
articleTitle: attached_template property
second_title: Aspose.Words for Python
description: "Document.attached_template property. Gets or sets the full path of the template attached to the document."
type: docs
weight: 20
url: /python-net/aspose.words/document/attached_template/
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
# Enable automatic style updating, but do not attach a template document.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Since there is no template document, the document had nowhere to track style changes.
# Use a SaveOptions object to automatically set a template
# if a document that we are saving does not have one.
options = aw.saving.SaveOptions.create_save_options('Document.default_template.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(ARTIFACTS_DIR + 'Document.default_template.docx', options)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* property [BuiltInDocumentProperties.template](../../../aspose.words.properties/builtindocumentproperties/template/)

