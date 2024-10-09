---
title: PdfDigitalSignatureDetails class
linktitle: PdfDigitalSignatureDetails class
articleTitle: PdfDigitalSignatureDetails class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureDetails class. Contains details for signing a PDF document with a digital signature."
type: docs
weight: 600
url: /python-net/aspose.words.saving/pdfdigitalsignaturedetails/
---

## PdfDigitalSignatureDetails class

Contains details for signing a PDF document with a digital signature.


### Remarks

At the moment digitally signing PDF documents is only available on .NET 3.5 or higher.

To digitally sign a PDF document when it is created by Aspose.Words, set the [PdfSaveOptions.digital_signature_details](../pdfsaveoptions/digital_signature_details/) 
property to a valid [PdfDigitalSignatureDetails](./) object and then save the document in the PDF format passing 
the [PdfSaveOptions](../pdfsaveoptions/) as a parameter into the [Document.save()](../../aspose.words/document/save/#str_saveoptions) method.

Aspose.Words creates a PKCS#7 signature over the whole PDF document and uses the "Adobe.PPKMS" filter and 
"adbe.pkcs7.sha1" subfilter when creating a digital signature.




### Constructors
| Name | Description |
| --- | --- |
| [PdfDigitalSignatureDetails()](./__init__/#default) | Initializes an instance of this class. |
| [PdfDigitalSignatureDetails(certificate_holder, reason, location, signature_date)](./__init__/#certificateholder_str_str_datetime) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [certificate_holder](./certificate_holder/) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [hash_algorithm](./hash_algorithm/) | Gets or sets the hash algorithm. |
| [location](./location/) | Gets or sets the location of the signing. |
| [reason](./reason/) | Gets or sets the reason for the signing. |
| [signature_date](./signature_date/) | Gets or sets the date of the signing. |
| [timestamp_settings](./timestamp_settings/) | Gets or sets the digital signature timestamp settings. |

### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + 'morzal.pfx', 'aw')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Configure the "digital_signature_details" object of the "SaveOptions" object to
# digitally sign the document as we render it with the "save" method.
signing_time = datetime.datetime.now()
import aspose.words.saving as aws
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'My Office', signing_time)
options.digital_signature_details.hash_algorithm = aw.saving.PdfDigitalSignatureHashAlgorithm.RIPE_MD160
self.assertEqual('Test Signing', options.digital_signature_details.reason)
self.assertEqual('My Office', options.digital_signature_details.location)
self.assertEqual(signing_time.astimezone(timezone.utc), options.digital_signature_details.signature_date)
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.pdf_digital_signature.pdf', options)
```

### See Also

* module [aspose.words.saving](../)
* property [PdfSaveOptions.digital_signature_details](../pdfsaveoptions/digital_signature_details/)

