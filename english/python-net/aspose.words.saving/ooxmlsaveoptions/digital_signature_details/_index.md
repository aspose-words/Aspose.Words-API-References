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
doc = aw.Document(MY_DIR + 'Document.docx')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + 'morzal.pfx', 'aw')
save_options = aw.saving.OoxmlSaveOptions()
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Some comments'
sign_options.sign_time = datetime.datetime.now()
save_options.digital_signature_details = aw.saving.DigitalSignatureDetails(certificate_holder, sign_options)
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.DigitalSignature.docx', save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

