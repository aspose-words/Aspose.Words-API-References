---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /de/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
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
# Fügen Sie einen relativen Hyperlink zu einem Dokument im lokalen Dateisystem mit dem Namen "Document.docx" ein.
# Durch Klicken auf den Link in Microsoft Word wird das vorgesehene Dokument geöffnet, sofern es verfügbar ist.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Dieser Link ist relativ. Wenn sich keine "Document.docx" im selben Ordner befindet
# wie das Dokument, das diesen Link enthält, wird der Link fehlerhaft sein.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# Das Dokument, zu dem wir verlinken möchten, befindet sich in einem anderen Verzeichnis als dem, in dem wir das Dokument speichern wollen.
# Wir könnten solche Links beheben, indem wir in jedem einen absoluten Dateinamen angeben.
# Alternativ könnten wir einen Basislink bereitstellen, den jeder Hyperlink mit einem relativen Dateinamen
# vor seinem Link anhängt, wenn wir darauf klicken.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

