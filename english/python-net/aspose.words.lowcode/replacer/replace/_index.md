﻿---
title: Replacer.replace method
linktitle: replace method
articleTitle: replace method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Replacer.replace method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/replacer/replace/
---

## replace(input_file_name, output_file_name, pattern, replacement) {#str_str_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file.


```python
def replace(self, input_file_name: str, output_file_name: str, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |

### Returns

The number of replacements made.


## replace(input_file_name, output_file_name, save_format, pattern, replacement) {#str_str_saveformat_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format.


```python
def replace(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |

### Returns

The number of replacements made.


## replace(input_file_name, output_file_name, save_format, pattern, replacement, options) {#str_str_saveformat_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options.


```python
def replace(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Returns

The number of replacements made.


## replace(input_file_name, output_file_name, save_options, pattern, replacement, options) {#str_str_saveoptions_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options.


```python
def replace(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Returns

The number of replacements made.


## replace(input_stream, output_stream, save_format, pattern, replacement) {#bytesio_bytesio_saveformat_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format.


```python
def replace(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |

### Returns

The number of replacements made.


## replace(input_stream, output_stream, save_format, pattern, replacement, options) {#bytesio_bytesio_saveformat_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format and additional options.


```python
def replace(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Returns

The number of replacements made.


## replace(input_stream, output_stream, save_options, pattern, replacement, options) {#bytesio_bytesio_saveoptions_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream, with the specified save format and additional options.


```python
def replace(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Returns

The number of replacements made.


## Examples

Shows how to replace string in the document.

```python
# There is a several ways to replace string in the document:
doc = MY_DIR + 'Footer.docx'
pattern = '(C)2006 Aspose Pty Ltd.'
replacement = 'Copyright (C) 2024 by Aspose Pty Ltd.'
options = aw.replacing.FindReplaceOptions()
options.find_whole_words_only = False
aw.lowcode.Replacer.replace(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.Replace.1.docx', pattern=pattern, replacement=replacement)
aw.lowcode.Replacer.replace(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.Replace.2.docx', save_format=aw.SaveFormat.DOCX, pattern=pattern, replacement=replacement)
aw.lowcode.Replacer.replace(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.Replace.3.docx', save_format=aw.SaveFormat.DOCX, pattern=pattern, replacement=replacement, options=options)
```

Shows how to replace string in the document using documents from the stream.

```python
# There is a several ways to replace string in the document using documents from the stream:
pattern = '(C)2006 Aspose Pty Ltd.'
replacement = 'Copyright (C) 2024 by Aspose Pty Ltd.'
with system_helper.io.FileStream(MY_DIR + 'Footer.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ReplaceStream.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Replacer.replace(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, pattern=pattern, replacement=replacement)
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ReplaceStream.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        options = aw.replacing.FindReplaceOptions()
        options.find_whole_words_only = False
        aw.lowcode.Replacer.replace(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, pattern=pattern, replacement=replacement, options=options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Replacer](../)

