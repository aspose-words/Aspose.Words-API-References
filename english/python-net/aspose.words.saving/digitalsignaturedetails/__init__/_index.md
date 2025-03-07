---
title: DigitalSignatureDetails constructor
linktitle: DigitalSignatureDetails constructor
articleTitle: DigitalSignatureDetails constructor
second_title: Aspose.Words for Python
description: "DigitalSignatureDetails constructor. Initializes a new instance of [DigitalSignatureDetails](../) class."
type: docs
weight: 10
url: /python-net/aspose.words.saving/digitalsignaturedetails/__init__/
---

## DigitalSignatureDetails(certificate_holder, sign_options) {#certificateholder_signoptions}

Initializes a new instance of [DigitalSignatureDetails](../) class.



```python
def __init__(self, certificate_holder: aspose.words.digitalsignatures.CertificateHolder, sign_options: aspose.words.digitalsignatures.SignOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| certificate_holder | [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/) | A certificate holder which contains the certificate itself. |
| sign_options | [SignOptions](../../../aspose.words.digitalsignatures/signoptions/) | Signature options to use for signing a document. |

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

