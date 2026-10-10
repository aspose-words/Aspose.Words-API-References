---
title: FileFormatInfo.has_digital_signature property
linktitle: has_digital_signature property
articleTitle: has_digital_signature property
second_title: Aspose.Words for Python
description: "FileFormatInfo.has_digital_signature property. Returns ``True`` if this document contains a digital signature"
type: docs
weight: 20
url: /it/python-net/aspose.words/fileformatinfo/has_digital_signature/
---

## FileFormatInfo.has_digital_signature property

Returns ``True`` if this document contains a digital signature.
This property merely informs that a digital signature is present on a document,
but it does not  specify whether the signature is valid or not.



```python
@property
def has_digital_signature(self) -> bool:
    ...

```

### Remarks

This property exists to help you sort documents that are digitally signed from those that are not.
If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will
be lost. This is by design because a digital signature exists to guard the authenticity of a document.
Using this property you can detect digitally signed documents before processing them in the same way as normal
documents and take some action to avoid losing the digital signature, for example notify the user.




### Examples

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

```python
# Usa un'istanza di FileFormatInfo per verificare che un documento non sia firmato digitalmente.
info = aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx')
self.assertEqual('.docx', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertFalse(info.has_digital_signature)
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx', cert_holder=certificate_holder, sign_options=sign_options)
# Usa una nuova istanza di FileFormatInstance per confermare che sia firmato.
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx')
self.assertTrue(info.has_digital_signature)
# Possiamo caricare e accedere alle firme di un documento firmato in una collezione come questa.
self.assertEqual(1, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx').count)
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)

