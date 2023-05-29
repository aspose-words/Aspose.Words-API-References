---
title: DigitalSignatureUtil.load_signatures method
linktitle: load_signatures method
articleTitle: load_signatures method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.load_signatures method"
type: docs
weight: 10
url: /python-net/aspose.words.digitalsignatures/digitalsignatureutil/load_signatures/
---

## load_signatures(file_name) {#str}

Loads digital signatures from document.


```python
def load_signatures(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## load_signatures(stream) {#bytesio}

Loads digital signatures from document using stream.


```python
def load_signatures(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## Examples

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

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

