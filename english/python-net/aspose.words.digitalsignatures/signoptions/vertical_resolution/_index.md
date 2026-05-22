---
title: SignOptions.vertical_resolution property
linktitle: vertical_resolution property
articleTitle: vertical_resolution property
second_title: Aspose.Words for Python
description: "SignOptions.vertical_resolution property. Gets or sets the vertical resolution for the digital signature"
type: docs
weight: 120
url: /python-net/aspose.words.digitalsignatures/signoptions/vertical_resolution/
---

## SignOptions.vertical_resolution property

Gets or sets the vertical resolution for the digital signature.
Default value is 1200.


```python
@property
def vertical_resolution(self) -> int:
    ...

@vertical_resolution.setter
def vertical_resolution(self, value: int):
    ...

```

### Examples

Shows how to sign a document with additional signing options.

```python
sign_options = aw.digitalsignatures.SignOptions()
sign_options.windows_version = '10.0'
sign_options.application_version = '16.0.19127'
sign_options.office_version = '16.0.19127/27'
sign_options.horizontal_resolution = 1024
sign_options.vertical_resolution = 768
sign_options.color_depth = 24
cert_bytes = system_helper.io.File.read_all_bytes(MY_DIR + 'morzal.pfx')
cert = aw.digitalsignatures.CertificateHolder.create(cert_bytes=cert_bytes, password='aw')
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.docx', cert_holder=cert, sign_options=sign_options)
signed_doc = aw.Document(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.docx')
signature = signed_doc.digital_signatures[0]
self.assertEqual(1, signed_doc.digital_signatures.count)
self.assertTrue(signature.is_valid)
self.assertEqual('10.0', signature.windows_version)
self.assertEqual('16.0.19127', signature.application_version)
self.assertEqual('16.0.19127/27', signature.office_version)
self.assertEqual(1024, signature.horizontal_resolution)
self.assertEqual(768, signature.vertical_resolution)
self.assertEqual(24, signature.color_depth)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

