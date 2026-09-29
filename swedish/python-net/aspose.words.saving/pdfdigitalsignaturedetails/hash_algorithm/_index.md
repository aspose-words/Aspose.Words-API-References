---
title: PdfDigitalSignatureDetails.hash_algorithm property
linktitle: hash_algorithm property
articleTitle: hash_algorithm property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.hash_algorithm property. Gets or sets the hash algorithm."
type: docs
weight: 30
url: /sv/python-net/aspose.words.saving/pdfdigitalsignaturedetails/hash_algorithm/
---

## PdfDigitalSignatureDetails.hash_algorithm property

Gets or sets the hash algorithm.


```python
@property
def hash_algorithm(self) -> aspose.words.saving.PdfDigitalSignatureHashAlgorithm:
    ...

@hash_algorithm.setter
def hash_algorithm(self, value: aspose.words.saving.PdfDigitalSignatureHashAlgorithm):
    ...

```

### Remarks

The default value is the SHA-256 algorithm.


### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Konfigurera "DigitalSignatureDetails" object av "SaveOptions" object för att
# signera dokumentet digitalt när vi renderar det med "Save"-metoden.
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

