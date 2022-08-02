---
title: detect_file_format method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.FileFormatUtil.detect_file_format method"
type: docs
weight: 30
url: /python-net/aspose.words/fileformatutil/detect_file_format/
---

## detect_file_format(file_name) {#str}

Detects and returns the information about a format of a document stored in a disk file.


```python
def detect_file_format(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

Even if this method detects the document format, it does not guarantee 
that the specified document is valid. This method only detects the document format by 
reading data that is sufficient for detection. To fully verify that a document is valid 
you need to load the document into a [Document](../../document/) object.

This method throws [FileCorruptedException](../../filecorruptedexception/) when the format is 
recognized, but the detection cannot complete because of corruption.




### Returns

A [FileFormatInfo](../../fileformatinfo/) object that contains the detected information.


## detect_file_format(stream) {#bytesio}

Detects and returns the information about a format of a document stored in a stream.


```python
def detect_file_format(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

The stream must be positioned at the beginning of the document.

When this method returns, the position in the stream is restored to the original position.

Even if this method detects the document format, it does not guarantee 
that the specified document is valid. This method only detects the document format by 
reading data that is sufficient for detection. To fully verify that a document is valid 
you need to load the document into a [Document](../../document/) object.

This method throws [FileCorruptedException](../../filecorruptedexception/) when the format is 
recognized, but the detection cannot complete because of corruption.




### Returns

A [FileFormatInfo](../../fileformatinfo/) object that contains the detected information.


## Examples

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

Shows how to use the aw.FileFormatUtil methods to detect the format of a document.

```python
# Load a document from a file that is missing a file extension, and then detect its file format.
with open(MY_DIR + "Word document with missing file extension", "rb") as doc_stream:

    info = aw.FileFormatUtil.detect_file_format(doc_stream)
    load_format = info.load_format

    self.assertEqual(aw.LoadFormat.DOC, load_format)

    # Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    # 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)

    # 2 -  Convert the LoadFormat directly to its SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)

    # Load a document from the stream, and then save it to the automatically detected file extension.
    doc = aw.Document(doc_stream)

    self.assertEqual(".doc", aw.FileFormatUtil.save_format_to_extension(save_format))

    doc.save(ARTIFACTS_DIR + "File.save_to_detected_file_format" + aw.FileFormatUtil.save_format_to_extension(save_format))
```

## See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

