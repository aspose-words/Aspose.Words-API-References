---
title: email property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets suggested signer's e-mail address"
type: docs
weight: 40
url: /python-net/aspose.words/signaturelineoptions/email/
---

## SignatureLineOptions.email property

Gets or sets suggested signer's e-mail address.
Default value for this property is **empty string** (System.String.Empty).



### Examples

Shows how to sign a document with a personal certificate and a signature line.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

signature_line_options = aw.SignatureLineOptions()
signature_line_options.signer = "vderyushev"
signature_line_options.signer_title = "QA"
signature_line_options.email = "vderyushev@aspose.com"
signature_line_options.show_date = True
signature_line_options.default_instructions = False
signature_line_options.instructions = "Please sign here."
signature_line_options.allow_comments = True

signature_line = builder.insert_signature_line(signature_line_options).signature_line
signature_line.provider_id = uuid.UUID("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2")

self.assertFalse(signature_line.is_signed)
self.assertFalse(signature_line.is_valid)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.signature_line_provider_id.docx")

sign_options = aw.digitalsignatures.SignOptions()
sign_options.signature_line_id = signature_line.id
sign_options.provider_id = signature_line.provider_id
sign_options.comments = "Document was signed by vderyushev"
sign_options.sign_time = datetime.utcnow()

cert_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

aw.digitalsignatures.DigitalSignatureUtil.sign(
    ARTIFACTS_DIR + "DocumentBuilder.signature_line_provider_id.docx",
    ARTIFACTS_DIR + "DocumentBuilder.signature_line_provider_id.signed.docx", cert_holder, sign_options)

# Re-open our saved document, and verify that the "is_signed" and "is_valid" properties both equal "True",
# indicating that the signature line contains a signature.
doc = aw.Document(ARTIFACTS_DIR + "DocumentBuilder.signature_line_provider_id.signed.docx")
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
signature_line = shape.signature_line

self.assertTrue(signature_line.is_signed)
self.assertTrue(signature_line.is_valid)
```

### See Also

* module [aspose.words](../../)
* class [SignatureLineOptions](../)

