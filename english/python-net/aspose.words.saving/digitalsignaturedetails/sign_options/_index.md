---
title: DigitalSignatureDetails.sign_options property
linktitle: sign_options property
articleTitle: sign_options property
second_title: Aspose.Words for Python
description: "DigitalSignatureDetails.sign_options property. Gets or sets a [DigitalSignatureDetails.sign_options](./) object used to sign a document."
type: docs
weight: 30
url: /python-net/aspose.words.saving/digitalsignaturedetails/sign_options/
---

## DigitalSignatureDetails.sign_options property

Gets or sets a [DigitalSignatureDetails.sign_options](./) object used to sign a document.



```python
@property
def sign_options(self) -> aspose.words.digitalsignatures.SignOptions:
    ...

@sign_options.setter
def sign_options(self, value: aspose.words.digitalsignatures.SignOptions):
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

