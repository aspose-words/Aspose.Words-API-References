---
title: PdfDigitalSignatureDetails.reason property
linktitle: reason property
articleTitle: reason property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.reason property. Gets or sets the reason for the signing."
type: docs
weight: 50
url: /python-net/aspose.words.saving/pdfdigitalsignaturedetails/reason/
---

## PdfDigitalSignatureDetails.reason property

Gets or sets the reason for the signing.

The default value is ``None``.



### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Contents of signed PDF.")

certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Configure the "digital_signature_details" object of the "SaveOptions" object to
# digitally sign the document as we render it with the "save" method.
signing_time = datetime.now()
import aspose.words.saving as aws
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, "Test Signing", "My Office", signing_time)
options.digital_signature_details.hash_algorithm = aw.saving.PdfDigitalSignatureHashAlgorithm.RIPE_MD160

self.assertEqual("Test Signing", options.digital_signature_details.reason)
self.assertEqual("My Office", options.digital_signature_details.location)
self.assertEqual(signing_time.astimezone(timezone.utc), options.digital_signature_details.signature_date)

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.pdf_digital_signature.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

