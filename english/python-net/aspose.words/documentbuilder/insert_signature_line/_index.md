---
title: DocumentBuilder.insert_signature_line method
linktitle: insert_signature_line method
articleTitle: insert_signature_line method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_signature_line method"
type: docs
weight: 450
url: /python-net/aspose.words/documentbuilder/insert_signature_line/
---

## insert_signature_line(signature_line_options) {#signaturelineoptions}

Inserts a signature line at the current position.


```python
def insert_signature_line(self, signature_line_options: aspose.words.SignatureLineOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| signature_line_options | [SignatureLineOptions](../../signaturelineoptions/) | The object that stores parameters of creating signature line. |

### Returns

The signature line node that was just inserted.


## insert_signature_line(signature_line_options, horz_pos, left, vert_pos, top, wrap_type) {#signaturelineoptions_relativehorizontalposition_float_relativeverticalposition_float_wraptype}

Inserts a signature line at the specified position.


```python
def insert_signature_line(self, signature_line_options: aspose.words.SignatureLineOptions, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| signature_line_options | [SignatureLineOptions](../../signaturelineoptions/) | The object that stores parameters of creating signature line. |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the signature line is measured from. |
| left | float | Distance in points from the origin to the left side of the signature line. |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the signature line measured from. |
| top | float | Distance in points from the origin to the top side of the signature line. |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the signature line. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The signature line node that was just inserted.


## Examples

Shows how to sign a document with a personal certificate and a signature line.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
signature_line_options = aw.SignatureLineOptions()
signature_line_options.signer = 'vderyushev'
signature_line_options.signer_title = 'QA'
signature_line_options.email = 'vderyushev@aspose.com'
signature_line_options.show_date = True
signature_line_options.default_instructions = False
signature_line_options.instructions = 'Please sign here.'
signature_line_options.allow_comments = True
signature_line = builder.insert_signature_line(signature_line_options).signature_line
signature_line.provider_id = uuid.UUID('CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2')
self.assertFalse(signature_line.is_signed)
self.assertFalse(signature_line.is_valid)
doc.save(ARTIFACTS_DIR + 'DocumentBuilder.signature_line_provider_id.docx')
sign_options = aw.digitalsignatures.SignOptions()
sign_options.signature_line_id = signature_line.id
sign_options.provider_id = signature_line.provider_id
sign_options.comments = 'Document was signed by vderyushev'
sign_options.sign_time = datetime.utcnow()
cert_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + 'morzal.pfx', 'aw')
aw.digitalsignatures.DigitalSignatureUtil.sign(ARTIFACTS_DIR + 'DocumentBuilder.signature_line_provider_id.docx', ARTIFACTS_DIR + 'DocumentBuilder.signature_line_provider_id.signed.docx', cert_holder, sign_options)
# Re-open our saved document, and verify that the "is_signed" and "is_valid" properties both equal "True",
# indicating that the signature line contains a signature.
doc = aw.Document(ARTIFACTS_DIR + 'DocumentBuilder.signature_line_provider_id.signed.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
signature_line = shape.signature_line
self.assertTrue(signature_line.is_signed)
self.assertTrue(signature_line.is_valid)
```

Shows how to insert an inline signature line into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
options = aw.SignatureLineOptions()
options.signer = 'John Doe'
options.signer_title = 'Manager'
options.email = 'johndoe@aspose.com'
options.show_date = True
options.default_instructions = False
options.instructions = 'Please sign here.'
options.allow_comments = True
builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=2, vert_pos=aw.drawing.RelativeVerticalPosition.PAGE, top=3, wrap_type=aw.drawing.WrapType.INLINE)
# The signature line can be signed in Microsoft Word by double clicking it.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SignatureLineInline.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

