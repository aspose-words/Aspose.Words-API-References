---
title: Watermarker.set_text method
linktitle: set_text method
articleTitle: set_text method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Watermarker.set_text method"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/watermarker/set_text/
---

## set_text(input_file_name, output_file_name, watermark_text) {#str_str_str}

Adds Text watermark into the document.


```python
def set_text(self, input_file_name: str, output_file_name: str, watermark_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| watermark_text | str | Text that is displayed as a watermark. |

## set_text(input_file_name, output_file_name, save_format, watermark_text) {#str_str_saveformat_str}

Adds Text watermark into the document.


```python
def set_text(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, watermark_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| watermark_text | str | Text that is displayed as a watermark. |

## set_text(input_stream, output_stream, save_format, watermark_text) {#bytesio_bytesio_saveformat_str}

Adds Text watermark into the document.


```python
def set_text(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, watermark_text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| watermark_text | str | Text that is displayed as a watermark. |

## set_text(input_file_name, output_file_name, watermark_text, options) {#str_str_str_textwatermarkoptions}

Adds Text watermark into the document.


```python
def set_text(self, input_file_name: str, output_file_name: str, watermark_text: str, options: aspose.words.TextWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| watermark_text | str | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

## set_text(input_file_name, output_file_name, save_format, watermark_text, options) {#str_str_saveformat_str_textwatermarkoptions}

Adds Text watermark into the document.


```python
def set_text(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, watermark_text: str, options: aspose.words.TextWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| watermark_text | str | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

## set_text(input_stream, output_stream, save_format, watermark_text, options) {#bytesio_bytesio_saveformat_str_textwatermarkoptions}

Adds Text watermark into the document.


```python
def set_text(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, watermark_text: str, options: aspose.words.TextWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| watermark_text | str | Text that is displayed as a watermark. |
| options | [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/) | Defines additional options for the text watermark. |

## Examples

Shows how to insert watermark text to the document.

```python
doc = MY_DIR + 'Big document.docx'
watermark_text = 'This is a watermark'
aw.lowcode.Watermarker.set_text(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.WatermarkText.1.docx', watermark_text=watermark_text)
aw.lowcode.Watermarker.set_text(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.WatermarkText.2.docx', save_format=aw.SaveFormat.DOCX, watermark_text=watermark_text)
watermark_options = aw.TextWatermarkOptions()
watermark_options.color = aspose.pydrawing.Color.red
aw.lowcode.Watermarker.set_text(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.WatermarkText.3.docx', watermark_text=watermark_text, options=watermark_options)
aw.lowcode.Watermarker.set_text(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.WatermarkText.4.docx', save_format=aw.SaveFormat.DOCX, watermark_text=watermark_text, options=watermark_options)
```

Shows how to insert watermark text to the document from the stream.

```python
watermark_text = 'This is a watermark'
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.WatermarkTextStream.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Watermarker.set_text(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, watermark_text=watermark_text)
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.WatermarkTextStream.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        options = aw.TextWatermarkOptions()
        options.color = aspose.pydrawing.Color.red
        aw.lowcode.Watermarker.set_text(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, watermark_text=watermark_text, options=options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Watermarker](../)

