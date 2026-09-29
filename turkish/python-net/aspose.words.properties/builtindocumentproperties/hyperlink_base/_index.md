---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /tr/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
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
# Yerel dosya sisteminde "Document.docx" adlı bir belgeye göreceli bir köprü (hyperlink) ekleyin.
# Microsoft Word'deki bağlantıya tıklamak, mevcutsa belirlenen belgeyi açar.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Bu bağlantı görecelidir. Aynı klasörde "Document.docx" yoksa
# bu bağlantıyı içeren belge olarak, bağlantı kırık olacaktır.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# Bağlantı vermeye çalıştığımız belge, belgeyi kaydetmeyi planladığımız dizinden farklı bir dizinde.
# Bağlantıları bu şekilde, her birine mutlak bir dosya adı ekleyerek düzeltebiliriz.
# Alternatif olarak, göreceli dosya adı içeren her hiperlinkin
# tıkladığımızda linkine ön ek olarak eklenecek bir temel bağlantı sağlayabiliriz.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

