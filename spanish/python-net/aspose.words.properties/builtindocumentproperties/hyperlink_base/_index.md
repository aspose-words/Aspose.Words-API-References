---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /es/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
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
builder = aw.DocumentBuilder(doc=doc)
# Inserte un hipervínculo relativo a un documento en el sistema de archivos local llamado "Document.docx".
# Al hacer clic en el enlace en Microsoft Word se abrirá el documento designado, si está disponible.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Este enlace es relativo. Si no hay "Document.docx" en la misma carpeta
# como el documento que contiene este enlace, el enlace quedará roto.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# El documento al que intentamos enlazar está en un directorio diferente al en el que planeamos guardar el documento.
# Podríamos corregir enlaces como este colocando un nombre de archivo absoluto en cada uno.
# Alternativamente, podríamos proporcionar un enlace base que cada hipervínculo con un nombre de archivo relativo
# anteponga a su enlace cuando hagamos clic en él.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

