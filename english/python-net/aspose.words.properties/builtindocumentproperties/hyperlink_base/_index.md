---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
---

## BuiltInDocumentProperties.hyperlink_base property

Specifies the base string used for evaluating relative hyperlinks in this document.


```python
@property
def hyperlink_base(self) -> str:
    ...

@hyperlink_base.setter
def hyperlink_base(self, value: str):
    ...

```

### Remarks

Aspose.Words does not use this property.




### Examples

Shows how to store the base part of a hyperlink in the document's properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a relative hyperlink to a document in the local file system named "Document.docx".
# Clicking on the link in Microsoft Word will open the designated document, if it is available.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# This link is relative. If there is no "Document.docx" in the same folder
# as the document that contains this link, the link will be broken.
self.assertFalse(os.path.exists(ARTIFACTS_DIR + 'Document.docx'))
doc.save(ARTIFACTS_DIR + 'DocumentProperties.hyperlink_base.broken_link.docx')
# The document we are trying to link to is in a different directory to the one we are planning to save the document in.
# We could fix links like this by putting an absolute filename in each one.
# Alternatively, we could provide a base link that every hyperlink with a relative filename
# will prepend to its link when we click on it.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(os.path.exists(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(ARTIFACTS_DIR + 'DocumentProperties.hyperlink_base.working_link.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

