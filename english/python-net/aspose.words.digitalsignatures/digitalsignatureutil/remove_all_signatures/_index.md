---
title: DigitalSignatureUtil.remove_all_signatures method
linktitle: remove_all_signatures method
articleTitle: remove_all_signatures method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.remove_all_signatures method"
type: docs
weight: 20
url: /python-net/aspose.words.digitalsignatures/digitalsignatureutil/remove_all_signatures/
---

## remove_all_signatures(src_file_name, dst_file_name) {#str_str}

Removes all digital signatures from source file and writes unsigned file to destination file.
The following formats are compatible for digital signature removal:
[LoadFormat.DOC](../../../aspose.words/loadformat/#DOC),
[LoadFormat.DOT](../../../aspose.words/loadformat/#DOT),
[LoadFormat.DOCX](../../../aspose.words/loadformat/#DOCX),
[LoadFormat.DOTX](../../../aspose.words/loadformat/#DOTX),
[LoadFormat.DOCM](../../../aspose.words/loadformat/#DOCM),
[LoadFormat.DOTM](../../../aspose.words/loadformat/#DOTM),
[LoadFormat.ODT](../../../aspose.words/loadformat/#ODT),
[LoadFormat.OTT](../../../aspose.words/loadformat/#OTT).




```python
def remove_all_signatures(self, src_file_name: str, dst_file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_file_name | str |  |
| dst_file_name | str |  |

## remove_all_signatures(src_stream, dst_stream) {#bytesio_bytesio}

Removes all digital signatures from document in source stream and writes unsigned document to destination stream.
**Output will be written to the start of stream and stream size will be updated with content length.**


The following formats are compatible for digital signature removal:
[LoadFormat.DOC](../../../aspose.words/loadformat/#DOC),
[LoadFormat.DOT](../../../aspose.words/loadformat/#DOT),
[LoadFormat.DOCX](../../../aspose.words/loadformat/#DOCX),
[LoadFormat.DOTX](../../../aspose.words/loadformat/#DOTX),
[LoadFormat.DOCM](../../../aspose.words/loadformat/#DOCM),
[LoadFormat.DOTM](../../../aspose.words/loadformat/#DOTM),
[LoadFormat.ODT](../../../aspose.words/loadformat/#ODT),
[LoadFormat.OTT](../../../aspose.words/loadformat/#OTT).




```python
def remove_all_signatures(self, src_stream: io.BytesIO, dst_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_stream | io.BytesIO |  |
| dst_stream | io.BytesIO |  |

## Examples

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

