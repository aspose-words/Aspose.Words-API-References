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
| file_name | str | Path to the document. |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## load_signatures(stream) {#bytesio}

Loads digital signatures from document using stream.


```python
def load_signatures(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream with the document. |

### Returns

Collection of digital signatures. Returns empty collection if file is not signed.


## Examples

Shows how to load signatures from a digitally signed document.

```python
# There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
# 1 -  Load from a document from a local file system filename:
digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=MY_DIR + 'Digitally signed.docx')
# If this collection is nonempty, then we can verify that the document is digitally signed.
self.assertEqual(1, digital_signatures.count)
# 2 -  Load from a document from a FileStream:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream:
    digital_signatures = aw.digitalsignatures.DigitalSignatureUtil.load_signatures(stream=stream)
    self.assertEqual(1, digital_signatures.count)
```

Shows how to remove digital signatures from a digitally signed document.

```python
# There are two ways of using the DigitalSignatureUtil class to remove digital signatures
# from a signed document by saving an unsigned copy of it somewhere else in the local file system.
# 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx')
# 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx', system_helper.io.FileMode.CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_stream=stream_in, dst_stream=stream_out)
# Verify that both our output documents have no digital signatures.
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx').count)
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx').count)
```

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

