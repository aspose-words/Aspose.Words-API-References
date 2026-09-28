---
title: SignatureLine.signer_title property
linktitle: signer_title property
articleTitle: signer_title property
second_title: Aspose.Words for Python
description: "SignatureLine.signer_title property. Gets or sets suggested signer's title (for example, Manager)"
type: docs
weight: 110
url: /de/python-net/aspose.words.drawing/signatureline/signer_title/
---

## SignatureLine.signer_title property

Gets or sets suggested signer's title (for example, Manager).
Default value for this property is **empty string** ().



```python
@property
def signer_title(self) -> str:
    ...

@signer_title.setter
def signer_title(self, value: str):
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
# Fügen Sie eine Form ein, die eine Signaturzeile enthält, deren Aussehen wir
# mithilfe des "SignatureLineOptions"-Objekts, das wir oben erstellt haben, anpassen.
# Wenn wir eine Form einfügen, deren Koordinaten in der rechten unteren Ecke der Seite beginnen,
# müssen wir negative x- und y-Koordinaten angeben, um die Form sichtbar zu machen.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# Überprüfen Sie die Eigenschaften unserer Signaturzeile über ihr Shape-Objekt.
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

