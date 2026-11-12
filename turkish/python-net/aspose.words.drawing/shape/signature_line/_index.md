---
title: Shape.signature_line property
linktitle: signature_line property
articleTitle: signature_line property
second_title: Aspose.Words for Python
description: "Shape.signature_line property. Gets [SignatureLine](../../signatureline/) object if the shape is a signature line"
type: docs
weight: 170
url: /tr/python-net/aspose.words.drawing/shape/signature_line/
---

## Shape.signature_line property

Gets [SignatureLine](../../signatureline/) object if the shape is a signature line. Returns ``None`` otherwise.



```python
@property
def signature_line(self) -> aspose.words.drawing.SignatureLine:
    ...

```

### Remarks

You can insert new [SignatureLine](../../signatureline/) into the document using [DocumentBuilder.insert_signature_line()](../../../aspose.words/documentbuilder/insert_signature_line/#signaturelineoptions) and



### Examples

Shows how to create a line for a signature and insert it into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
options = aw.SignatureLineOptions()
options.allow_comments = True
options.default_instructions = True
options.email = 'john.doe@management.com'
options.instructions = 'Please sign here'
options.show_date = True
options.signer = 'John Doe'
options.signer_title = 'Senior Manager'
# İmza satırı içerecek bir şekil ekleyin, görünümünü
# yukarıda oluşturduğumuz "SignatureLineOptions" nesnesiyle özelleştireceğiz.
# Eğer bir şeklin koordinatları sayfanın sağ alt köşesinden başlıyorsa,
# şekli görünür hâle getirmek için negatif x ve y koordinatları sağlamamız gerekir.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# İmza satırımızın özelliklerini Shape nesnesi aracılığıyla doğrulayın.
signature_line = shape.signature_line
self.assertEqual('john.doe@management.com', signature_line.email)
self.assertEqual('John Doe', signature_line.signer)
self.assertEqual('Senior Manager', signature_line.signer_title)
self.assertEqual('Please sign here', signature_line.instructions)
self.assertTrue(signature_line.show_date)
self.assertTrue(signature_line.allow_comments)
self.assertTrue(signature_line.default_instructions)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.SignatureLine.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)
* method [DocumentBuilder.insert_signature_line()](../../../aspose.words/documentbuilder/insert_signature_line/#signaturelineoptions_relativehorizontalposition_float_relativeverticalposition_float_wraptype)

