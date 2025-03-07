---
title: DigitalSignatureDetails class
linktitle: DigitalSignatureDetails class
articleTitle: DigitalSignatureDetails class
second_title: Aspose.Words for Python
description: "aspose.words.saving.DigitalSignatureDetails class. Contains details for signing a document with a digital signature."
type: docs
weight: 60
url: /python-net/aspose.words.saving/digitalsignaturedetails/
---

## DigitalSignatureDetails class

Contains details for signing a document with a digital signature.


### Constructors
| Name | Description |
| --- | --- |
| [DigitalSignatureDetails(certificate_holder, sign_options)](./__init__/#certificateholder_signoptions) | Initializes a new instance of [DigitalSignatureDetails](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [certificate_holder](./certificate_holder/) | Gets or sets a [DigitalSignatureDetails.certificate_holder](./certificate_holder/) object that contains the certificate used to sign a document. |
| [sign_options](./sign_options/) | Gets or sets a [DigitalSignatureDetails.sign_options](./sign_options/) object used to sign a document. |

### Examples

Shows how to sign OOXML document.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Some comments'
sign_options.sign_time = datetime.datetime.now()
digital_signature_details = aw.saving.DigitalSignatureDetails(certificate_holder, sign_options)
save_options = aw.saving.OoxmlSaveOptions()
save_options.digital_signature_details = digital_signature_details
self.assertEqual(certificate_holder, digital_signature_details.certificate_holder)
self.assertEqual('Some comments', digital_signature_details.sign_options.comments)
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.DigitalSignature.docx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

