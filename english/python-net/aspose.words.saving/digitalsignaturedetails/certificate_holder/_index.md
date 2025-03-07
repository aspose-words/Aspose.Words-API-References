---
title: DigitalSignatureDetails.certificate_holder property
linktitle: certificate_holder property
articleTitle: certificate_holder property
second_title: Aspose.Words for Python
description: "DigitalSignatureDetails.certificate_holder property. Gets or sets a [DigitalSignatureDetails.certificate_holder](./) object that contains the certificate used to sign a document."
type: docs
weight: 20
url: /python-net/aspose.words.saving/digitalsignaturedetails/certificate_holder/
---

## DigitalSignatureDetails.certificate_holder property

Gets or sets a [DigitalSignatureDetails.certificate_holder](./) object that contains the certificate used to sign a document.



```python
@property
def certificate_holder(self) -> aspose.words.digitalsignatures.CertificateHolder:
    ...

@certificate_holder.setter
def certificate_holder(self, value: aspose.words.digitalsignatures.CertificateHolder):
    ...

```

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

* module [aspose.words.saving](../../)
* class [DigitalSignatureDetails](../)

