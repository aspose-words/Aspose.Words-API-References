﻿---
title: SignatureLine class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to signature line properties"
type: docs
weight: 350
url: /python-net/aspose.words.drawing/signatureline/
---

## SignatureLine class

Provides access to signature line properties.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [allow_comments](./allow_comments/) | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is ``False``. |
| [default_instructions](./default_instructions/) | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is ``True``. |
| [email](./email/) | Gets or sets suggested signer's e-mail address.  Default value for this property is **empty string** (System.String.Empty). |
| [id](./id/) | Gets or sets identifier for this signature line. This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). This value must be unique and by default it is randomly generated new Guid (System.Guid.NewGuid). |
| [instructions](./instructions/) | Gets or sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [SignatureLine.default_instructions](./default_instructions/) is set. Default value for this property is **empty string** (System.String.Empty). |
| [is_signed](./is_signed/) | Indicates that signature line is signed by digital signature. |
| [is_valid](./is_valid/) | Indicates that signature line is signed by digital signature and this digital signature is valid. |
| [provider_id](./provider_id/) | Gets or sets signature provider identifier for this signature line. Default value is "{00000000-0000-0000-0000-000000000000}". |
| [show_date](./show_date/) | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is ``True``. |
| [signer](./signer/) | Gets or sets suggested signer of the signature line. Default value for this property is **empty string** (System.String.Empty). |
| [signer_title](./signer_title/) | Gets or sets suggested signer's title (for example, Manager). Default value for this property is **empty string** (System.String.Empty). |

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

* module [aspose.words.drawing](../)

