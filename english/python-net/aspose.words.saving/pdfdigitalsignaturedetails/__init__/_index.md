---
title: PdfDigitalSignatureDetails constructor
linktitle: PdfDigitalSignatureDetails constructor
articleTitle: PdfDigitalSignatureDetails constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureDetails constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/pdfdigitalsignaturedetails/__init__/
---

## PdfDigitalSignatureDetails() {#default}

Initializes an instance of this class.


```python
def __init__(self):
    ...
```

## PdfDigitalSignatureDetails(certificate_holder, reason, location, signature_date) {#certificateholder_str_str_datetime}

Initializes an instance of this class.


```python
def __init__(self, certificate_holder: aspose.words.digitalsignatures.CertificateHolder, reason: str, location: str, signature_date: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| certificate_holder | [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/) | A certificate holder which contains the certificate itself. |
| reason | str | The reason for signing. |
| location | str | The location of signing. |
| signature_date | datetime.datetime | The date and time of signing. |

## Examples

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

## See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

