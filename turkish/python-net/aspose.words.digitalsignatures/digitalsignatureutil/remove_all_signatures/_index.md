---
title: DigitalSignatureUtil.remove_all_signatures method
linktitle: remove_all_signatures method
articleTitle: remove_all_signatures method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.remove_all_signatures method"
type: docs
weight: 20
url: /tr/python-net/aspose.words.digitalsignatures/digitalsignatureutil/remove_all_signatures/
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
# DigitalSignatureUtil sınıfını kullanarak dijital imzaları kaldırmanın iki yolu vardır
# İmzalı bir belgeden, imzasız bir kopyasını yerel dosya sisteminde başka bir yere kaydederek.
# 1 - İmzalı belge ve imzasız kopyanın konumlarını dosya adı dizeleriyle belirleyin:
aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx')
# 2 - İmzalı belge ve imzasız kopyanın konumlarını dosya akışlarıyla belirleyin:
with system_helper.io.FileStream(MY_DIR + 'Digitally signed.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx', system_helper.io.FileMode.CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.remove_all_signatures(src_stream=stream_in, dst_stream=stream_out)
# Her iki çıktı belgemizin de dijital imza içermediğini doğrulayın.
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromString.docx').count)
self.assertEqual(0, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.LoadAndRemove.FromStream.docx').count)
```

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

