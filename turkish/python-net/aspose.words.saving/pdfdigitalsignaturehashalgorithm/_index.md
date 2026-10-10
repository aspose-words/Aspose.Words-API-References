---
title: PdfDigitalSignatureHashAlgorithm enumeration
linktitle: PdfDigitalSignatureHashAlgorithm enumeration
articleTitle: PdfDigitalSignatureHashAlgorithm enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureHashAlgorithm enumeration. Specifies a digital hash algorithm used by a digital signature."
type: docs
weight: 660
url: /tr/python-net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
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

### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# "SaveOptions" nesnesinin "DigitalSignatureDetails" nesnesini yapılandırarak
# "Save" yöntemiyle belgeyi işlerken dijital olarak imzalayın.
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

* module [aspose.words.saving](../)

