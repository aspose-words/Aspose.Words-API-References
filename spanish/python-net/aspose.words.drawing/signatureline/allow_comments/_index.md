---
title: SignatureLine.allow_comments property
linktitle: allow_comments property
articleTitle: allow_comments property
second_title: Aspose.Words for Python
description: "SignatureLine.allow_comments property. Gets or sets a value indicating that the signer can add comments in the Sign dialog"
type: docs
weight: 10
url: /es/python-net/aspose.words.drawing/signatureline/allow_comments/
---

## SignatureLine.allow_comments property

Gets or sets a value indicating that the signer can add comments in the Sign dialog.
Default value for this property is ``False``.



```python
@property
def allow_comments(self) -> bool:
    ...

@allow_comments.setter
def allow_comments(self, value: bool):
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
# Insertar una forma que contendrá una línea de firma, cuya apariencia vamos a
# personalizar usando el objeto "SignatureLineOptions" que hemos creado arriba.
# Si insertamos una forma cuyas coordenadas se originan en la esquina inferior derecha de la página,
# necesitaremos proporcionar coordenadas x e y negativas para que la forma sea visible.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# Verifique las propiedades de nuestra línea de firma a través de su objeto Shape.
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

