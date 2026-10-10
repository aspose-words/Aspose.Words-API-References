---
title: SignatureLine.default_instructions property
linktitle: default_instructions property
articleTitle: default_instructions property
second_title: Aspose.Words for Python
description: "SignatureLine.default_instructions property. Gets or sets a value indicating that default instructions is shown in the Sign dialog"
type: docs
weight: 20
url: /fr/python-net/aspose.words.drawing/signatureline/default_instructions/
---

## SignatureLine.default_instructions property

Gets or sets a value indicating that default instructions is shown in the Sign dialog.
Default value for this property is ``True``.



```python
@property
def default_instructions(self) -> bool:
    ...

@default_instructions.setter
def default_instructions(self, value: bool):
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
# Insérer une forme qui contiendra une ligne de signature, dont l'apparence sera
# personnalisée à l'aide de l'objet "SignatureLineOptions" que nous avons créé ci‑dessus.
# Si nous insérons une forme dont les coordonnées proviennent du coin inférieur droit de la page,
# nous devrons fournir des coordonnées x et y négatives pour faire apparaître la forme.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# Vérifiez les propriétés de notre ligne de signature via son objet Shape.
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

