---
title: SignatureLine.allow_comments property
linktitle: allow_comments property
articleTitle: allow_comments property
second_title: Aspose.Words for Python
description: "SignatureLine.allow_comments property. Gets or sets a value indicating that the signer can add comments in the Sign dialog"
type: docs
weight: 10
url: /python-net/aspose.words.drawing/signatureline/allow_comments/
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
builder = aw.DocumentBuilder(doc)

options = aw.SignatureLineOptions()
options.allow_comments = True
options.default_instructions = True
options.email = "john.doe@management.com"
options.instructions = "Please sign here"
options.show_date = True
options.signer = "John Doe"
options.signer_title = "Senior Manager"

# Insert a shape that will contain a signature line, whose appearance we will
# customize using the "SignatureLineOptions" object we have created above.
# If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
# we will need to supply negative x and y coordinates to bring the shape into view.
shape = builder.insert_signature_line(options, aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
    aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, aw.drawing.WrapType.NONE)

self.assertTrue(shape.is_signature_line)

# Verify the properties of our signature line via its Shape object.
signature_line = shape.signature_line

self.assertEqual("john.doe@management.com", signature_line.email)
self.assertEqual("John Doe", signature_line.signer)
self.assertEqual("Senior Manager", signature_line.signer_title)
self.assertEqual("Please sign here", signature_line.instructions)
self.assertTrue(signature_line.show_date)
self.assertTrue(signature_line.allow_comments)
self.assertTrue(signature_line.default_instructions)

doc.save(ARTIFACTS_DIR + "Shape.signature_line.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [SignatureLine](../)

