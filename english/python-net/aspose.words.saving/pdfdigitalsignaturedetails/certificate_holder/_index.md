---
title: PdfDigitalSignatureDetails.certificate_holder property
linktitle: certificate_holder property
articleTitle: certificate_holder property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.certificate_holder property. Returns the certificate holder object that contains the certificate was used to sign the document."
type: docs
weight: 20
url: /python-net/aspose.words.saving/pdfdigitalsignaturedetails/certificate_holder/
---

## PdfDigitalSignatureDetails.certificate_holder property

Returns the certificate holder object that contains the certificate was used to sign the document.


```python
@property
def certificate_holder(self) -> aspose.words.digitalsignatures.CertificateHolder:
    ...

@certificate_holder.setter
def certificate_holder(self, value: aspose.words.digitalsignatures.CertificateHolder):
    ...

```

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
self.assertEqual(signing_time, options.digital_signature_details.signature_date)
self.assertEqual(certificate_holder, options.digital_signature_details.certificate_holder)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignature.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

