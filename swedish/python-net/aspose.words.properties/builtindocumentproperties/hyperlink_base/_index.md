---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /sv/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
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
# Infoga en relativ hyperlänk till ett dokument i det lokala filsystemet med namnet "Document.docx".
# Att klicka på länken i Microsoft Word öppnar det angivna dokumentet, om det är tillgängligt.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Den här länken är relativ. Om det inte finns någon "Document.docx" i samma mapp
# som dokumentet som innehåller länken, kommer länken att vara trasig.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# Dokumentet vi försöker länka till ligger i en annan katalog än den vi planerar att spara dokumentet i.
# Vi kan åtgärda länkar som dessa genom att ange ett absolut filnamn i varje länk.
# Alternativt kan vi tillhandahålla en baslänk som varje hyperlänk med ett relativt filnamn
# kommer att lägga till i början av sin länk när vi klickar på den.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

