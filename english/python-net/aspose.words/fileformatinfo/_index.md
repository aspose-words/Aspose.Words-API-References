---
title: FileFormatInfo class
linktitle: FileFormatInfo class
articleTitle: FileFormatInfo class
second_title: Aspose.Words for Python
description: "aspose.words.FileFormatInfo class. Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods"
type: docs
weight: 400
url: /python-net/aspose.words/fileformatinfo/
---

## FileFormatInfo class

Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods.
To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/python-net/detect-file-format-and-check-format-compatibility/) documentation article.




### Remarks

You do not create instances of this class directly. Objects of this class are returned by
[FileFormatUtil.detect_file_format()](../fileformatutil/detect_file_format/#bytesio) methods.




### Properties

| Name | Description |
| --- | --- |
| [encoding](./encoding/) | Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents. |
| [has_digital_signature](./has_digital_signature/) | Returns ``True`` if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not  specify whether the signature is valid or not. |
| [has_macros](./has_macros/) | Returns ``True`` if this document contains a VBA macros. |
| [is_encrypted](./is_encrypted/) | Returns ``True`` if the document is encrypted and requires a password to open. |
| [load_format](./load_format/) | Gets the detected document format. |

### Examples

Shows how to use the aw.FileFormatUtil class to detect the document format and encryption.

```python
doc = aw.Document()

# Configure a SaveOptions object to encrypt the document
# with a password when we save it, and then save the document.
save_options = aw.saving.OdtSaveOptions(aw.SaveFormat.ODT)
save_options.password = "MyPassword"

doc.save(ARTIFACTS_DIR + "File.detect_document_encryption.odt", save_options)

# Verify the file type of our document, and its encryption status.
info = aw.FileFormatUtil.detect_file_format(ARTIFACTS_DIR + "File.detect_document_encryption.odt")

self.assertEqual(".odt", aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertTrue(info.is_encrypted)
```

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

* module [aspose.words](../)

