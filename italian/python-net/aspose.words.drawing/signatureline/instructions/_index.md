---
title: SignatureLine.instructions property
linktitle: instructions property
articleTitle: instructions property
second_title: Aspose.Words for Python
description: "SignatureLine.instructions property. Gets or sets instructions to the signer that are displayed on signing the signature line"
type: docs
weight: 50
url: /it/python-net/aspose.words.drawing/signatureline/instructions/
---

## SignatureLine.instructions property

Gets or sets instructions to the signer that are displayed on signing the signature line.
This property is ignored if [SignatureLine.default_instructions](../default_instructions/) is set.
Default value for this property is **empty string** ().



```python
@property
def instructions(self) -> str:
    ...

@instructions.setter
def instructions(self, value: str):
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
# Inserisci una forma che conterrà una linea di firma, la cui apparenza noi
# personalizzeremo usando l'oggetto "SignatureLineOptions" che abbiamo creato sopra.
# Se inseriamo una forma le cui coordinate originano dall'angolo inferiore destro della pagina,
# dovremo fornire coordinate x e y negative per portare la forma in vista.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# Verifica le proprietà della nostra linea di firma tramite il suo oggetto Shape.
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

