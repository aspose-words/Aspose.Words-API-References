---
title: PdfDigitalSignatureDetails.signature_date property
linktitle: signature_date property
articleTitle: signature_date property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.signature_date property. Gets or sets the date of the signing."
type: docs
weight: 60
url: /es/python-net/aspose.words.saving/pdfdigitalsignaturedetails/signature_date/
---

## PdfDigitalSignatureDetails.signature_date property

Gets or sets the date of the signing.


```python
@property
def signature_date(self) -> datetime.datetime:
    ...

@signature_date.setter
def signature_date(self, value: datetime.datetime):
    ...

```

### Remarks

The default value is the current time.

This value will appear in the digital signature as an unverified computer time.




### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Configure el objeto "DigitalSignatureDetails" del objeto "SaveOptions" para
# firmar digitalmente el documento mientras lo renderizamos con el método "Save".
signing_time = datetime.datetime(2015, 7, 20)
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'My Office', signing_time)
options.digital_signature_details.hash_algorithm = aw.saving.PdfDigitalSignatureHashAlgorithm.RIPE_MD160
self.assertEqual('Test Signing', options.digital_signature_details.reason)
self.assertEqual('My Office', options.digital_signature_details.location)
self.assertEqual(signing_time, options.digital_signature_details.signature_date.replace(tzinfo=None))
self.assertEqual(certificate_holder, options.digital_signature_details.certificate_holder)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignature.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

