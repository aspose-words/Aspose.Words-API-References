---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /it/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
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
# Inserisci un collegamento ipertestuale relativo a un documento nel file system locale denominato "Document.docx".
# Fare clic sul collegamento in Microsoft Word aprirà il documento designato, se è disponibile.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Questo collegamento è relativo. Se non c'è "Document.docx" nella stessa cartella
# come il documento che contiene questo collegamento, il collegamento sarà interrotto.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# Il documento a cui stiamo cercando di collegarci si trova in una directory diversa da quella in cui prevediamo di salvare il documento.
# Potremmo correggere i collegamenti in questo modo inserendo un nome file assoluto in ciascuno.
# In alternativa, potremmo fornire un collegamento base a cui ogni hyperlink con un nome file relativo
# verrà anteposto al suo collegamento quando ci clicchiamo sopra.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

