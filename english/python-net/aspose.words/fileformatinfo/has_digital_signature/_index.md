---
title: has_digital_signature property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns true if this document contains a digital signature"
type: docs
weight: 20
url: /python-net/aspose.words/fileformatinfo/has_digital_signature/
---

## FileFormatInfo.has_digital_signature property

Returns true if this document contains a digital signature. 
This property merely informs that a digital signature is present on a document, 
but it does not  specify whether the signature is valid or not.

This property exists to help you sort documents that are digitally signed from those that are not.
If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will 
be lost. This is by design because a digital signature exists to guard the authenticity of a document. 
Using this property you can detect digitally signed documents before processing them in the same way as normal 
documents and take some action to avoid losing the digital signature, for example notify the user.




### Examples

Shows how to use the aw.FileFormatUtil class to detect the document format and presence of digital signatures.

```python
# Use a FileFormatInfo instance to verify that a document is not digitally signed.
info = aw.FileFormatUtil.detect_file_format(MY_DIR + "Document.docx")

self.assertEqual(".docx", aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertFalse(info.has_digital_signature)

sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.now()

certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw", None)
aw.digitalsignatures.DigitalSignatureUtil.sign(MY_DIR + "Document.docx", ARTIFACTS_DIR + "File.detect_digital_signatures.docx",
    certificate_holder, sign_options)

# Use a new FileFormatInstance to confirm that it is signed.
info = aw.FileFormatUtil.detect_file_format(ARTIFACTS_DIR + "File.detect_digital_signatures.docx")

self.assertTrue(info.has_digital_signature)

# We can load and access the signatures of a signed document in a collection like this.
self.assertEqual(1, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(ARTIFACTS_DIR + "File.detect_digital_signatures.docx").count)
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)

