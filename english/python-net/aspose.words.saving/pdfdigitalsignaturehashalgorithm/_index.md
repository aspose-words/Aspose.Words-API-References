---
title: PdfDigitalSignatureHashAlgorithm enumeration
linktitle: PdfDigitalSignatureHashAlgorithm enumeration
articleTitle: PdfDigitalSignatureHashAlgorithm enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureHashAlgorithm enumeration. Specifies a digital hash algorithm used by a digital signature."
type: docs
weight: 13200
url: /python-net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---

## PdfDigitalSignatureHashAlgorithm enumeration

Specifies a digital hash algorithm used by a digital signature.


### Members

| Name | Description |
| --- | --- |
| SHA256 | SHA-256 hash algorithm. |
| SHA384 | SHA-384 hash algorithm. |
| SHA512 | SHA-512 hash algorithm. |
| RIPE_MD160 | RIPEMD-160 hash algorithm. |
| AUTO | Automatically selects an appropriate hash algorithm based on the provided private key. |

### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
# digitally sign the document as we render it with the "Save" method.
signing_time = datetime.datetime(2015, 7, 20)
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'My Office', signing_time)
options.digital_signature_details.hash_algorithm = aw.saving.PdfDigitalSignatureHashAlgorithm.RIPE_MD160
self.assertEqual('Test Signing', options.digital_signature_details.reason)
self.assertEqual('My Office', options.digital_signature_details.location)
self.assertEqual(signing_time, options.digital_signature_details.signature_date.replace(tzinfo=None))
self.assertEqual(certificate_holder, options.digital_signature_details.certificate_holder)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignature.pdf', save_options=options)
```

Shows how to sign a PDF document with a hash algorithm selected automatically based on the private key.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Contents of signed PDF.")
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + "morzal.pfx",
                                                                   password="aw")
options = aw.saving.PdfSaveOptions()
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, "Test Signing",
                                                                         "My Office", datetime.datetime.now())
# "Auto" is the default value. Some newer digital signature algorithms have specific digest requirements,
# so Aspose.Words picks a hash algorithm that is compatible with the certificate's private key.
self.assertEqual(aw.saving.PdfDigitalSignatureHashAlgorithm.AUTO,
                 options.digital_signature_details.hash_algorithm)
doc.save(file_name=ARTIFACTS_DIR + "PdfSaveOptions.PdfDigitalSignatureAutoHashAlgorithm.pdf",
         save_options=options)
```

### See Also

* module [aspose.words.saving](../)

