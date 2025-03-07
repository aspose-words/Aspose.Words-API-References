---
title: OoxmlSaveOptions.digital_signature_details property
linktitle: digital_signature_details property
articleTitle: digital_signature_details property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.digital_signature_details property. Gets or sets [DigitalSignatureDetails](../../digitalsignaturedetails/) object used to sign a document."
type: docs
weight: 40
url: /python-net/aspose.words.saving/ooxmlsaveoptions/digital_signature_details/
---

## OoxmlSaveOptions.digital_signature_details property

Gets or sets [DigitalSignatureDetails](../../digitalsignaturedetails/) object used to sign a document.



```python
@property
def digital_signature_details(self) -> aspose.words.saving.DigitalSignatureDetails:
    ...

@digital_signature_details.setter
def digital_signature_details(self, value: aspose.words.saving.DigitalSignatureDetails):
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
* class [OoxmlSaveOptions](../)

