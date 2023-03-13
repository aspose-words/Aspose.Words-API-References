﻿---
title: DigitalSignatureUtil class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides methods for signing document"
type: docs
weight: 50
url: /python-net/aspose.words.digitalsignatures/digitalsignatureutil/
---

## DigitalSignatureUtil class

Provides methods for signing document.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article.




Since digital signature works with file content rather than Document Object Model these methods are put into a separate class.

Supported formats are [LoadFormat.DOC](../../aspose.words/loadformat/#DOC) and [LoadFormat.DOCX](../../aspose.words/loadformat/#DOCX).




### Methods

| Name | Description |
| --- | --- |
|[ load_signatures(file_name)](./load_signatures/#str) | Loads digital signatures from document. |
|[ load_signatures(stream)](./load_signatures/#bytesio) | Loads digital signatures from document using stream. |
|[ remove_all_signatures(src_file_name, dst_file_name)](./remove_all_signatures/#str_str) | Removes all digital signatures from source file and writes unsigned file to destination file. |
|[ remove_all_signatures(src_stream, dst_stream)](./remove_all_signatures/#bytesio_bytesio) | Removes all digital signatures from document in source stream and writes unsigned document to destination stream. **Output will be written to the start of stream and stream size will be updated with content length.** |
|[ sign(src_stream, dst_stream, cert_holder, sign_options)](./sign/#bytesio_bytesio_certificateholder_signoptions) | Signs source document using given [CertificateHolder](../certificateholder/) and [SignOptions](../signoptions/)  with digital signature and writes signed document to destination stream. Document should be either [LoadFormat.DOC](../../aspose.words/loadformat/#DOC) or [LoadFormat.DOCX](../../aspose.words/loadformat/#DOCX). |
|[ sign(src_file_name, dst_file_name, cert_holder, sign_options)](./sign/#str_str_certificateholder_signoptions) | Signs source document using given [CertificateHolder](../certificateholder/) and [SignOptions](../signoptions/) with digital signature and writes signed document to destination file. Document should be either [LoadFormat.DOC](../../aspose.words/loadformat/#DOC) or [LoadFormat.DOCX](../../aspose.words/loadformat/#DOCX). |
|[ sign(src_stream, dst_stream, cert_holder)](./sign/#bytesio_bytesio_certificateholder) | Signs source document using given [CertificateHolder](../certificateholder/) with digital signature and writes signed document to destination stream. Document should be either [LoadFormat.DOC](../../aspose.words/loadformat/#DOC) or [LoadFormat.DOCX](../../aspose.words/loadformat/#DOCX). |
|[ sign(src_file_name, dst_file_name, cert_holder)](./sign/#str_str_certificateholder) | Signs source document using given [CertificateHolder](../certificateholder/) with digital signature and writes signed document to destination file. Document should be either [LoadFormat.DOC](../../aspose.words/loadformat/#DOC) or [LoadFormat.DOCX](../../aspose.words/loadformat/#DOCX). |

### Examples

Shows how to load signatures from a digitally signed document.

```python
# There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
# 1 -  Load from a document from a local file system filename:
digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(MY_DIR + "Digitally signed.docx")

# If this collection is nonempty, then we can verify that the document is digitally signed.
self.assertEqual(1, digital_signatures.count)

# 2 -  Load from a document from a FileStream:
with open(MY_DIR + "Digitally signed.docx", "rb") as stream:
    digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(stream)
    self.assertEqual(1, digital_signatures.count)
```

Shows how to remove digital signatures from a digitally signed document.

```python
# There are two ways of using the DigitalSignatureUtil class to remove digital signatures
# from a signed document by saving an unsigned copy of it somewhere else in the local file system.
# 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(
    MY_DIR + "Digitally signed.docx",
    ARTIFACTS_DIR + "DigitalSignatureUtil.load_and_remove.from_string.docx")

# 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
with open(MY_DIR + "Digitally signed.docx", "rb") as stream_in:
    with open(ARTIFACTS_DIR + "DigitalSignatureUtil.load_and_remove.from_stream.docx", "wb") as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(stream_in, stream_out)

# Verify that both our output documents have no digital signatures.
self.assertListEqual([], aw.digitalsignatures.DigitalSignatureUtil.load_signatures(ARTIFACTS_DIR + "DigitalSignatureUtil.load_and_remove.from_string.docx"))
self.assertListEqual([], aw.digitalsignatures.DigitalSignatureUtil.load_signatures(ARTIFACTS_DIR + "DigitalSignatureUtil.load_and_remove.from_stream.docx"))
```

### See Also

* module [aspose.words.digitalsignatures](../)

