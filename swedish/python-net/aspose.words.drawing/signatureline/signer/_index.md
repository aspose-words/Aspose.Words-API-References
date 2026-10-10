---
title: SignatureLine.signer property
linktitle: signer property
articleTitle: signer property
second_title: Aspose.Words for Python
description: "SignatureLine.signer property. Gets or sets suggested signer of the signature line"
type: docs
weight: 100
url: /sv/python-net/aspose.words.drawing/signatureline/signer/
---

## SignatureLine.signer property

Gets or sets suggested signer of the signature line.
Default value for this property is **empty string** ().



```python
@property
def signer(self) -> str:
    ...

@signer.setter
def signer(self, value: str):
    ...

```

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
# Infoga en form som kommer att innehålla en signaturlinje, vars utseende vi kommer att
# anpassa med hjälp av objektet "SignatureLineOptions" som vi har skapat ovan.
# Om vi infogar en form vars koordinater har sitt ursprung i sidans nedre högra hörn,
# måste vi ange negativa x- och y-koordinater för att få formen att visas.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# Verifiera egenskaperna för vår signaturlinje via dess Shape-objekt.
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
* class [SignatureLine](../)

