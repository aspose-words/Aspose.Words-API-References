---
title: Replacer.replace_regex method
linktitle: replace_regex method
articleTitle: replace_regex method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Replacer.replace_regex method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/replacer/replace_regex/
---

## replace_regex(input_file_name, output_file_name, pattern, replacement) {#str_str_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression.


```python
def replace_regex(self, input_file_name: str, output_file_name: str, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




### Returns

The number of replacements made.


## replace_regex(input_file_name, output_file_name, save_format, pattern, replacement) {#str_str_saveformat_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




### Returns

The number of replacements made.


## replace_regex(input_file_name, output_file_name, save_format, pattern, replacement, options) {#str_str_saveformat_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




### Returns

The number of replacements made.


## replace_regex(input_file_name, output_file_name, save_options, pattern, replacement) {#str_str_saveoptions_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




### Returns

The number of replacements made.


## replace_regex(input_file_name, output_file_name, save_options, pattern, replacement, options) {#str_str_saveoptions_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




### Returns

The number of replacements made.


## replace_regex(input_stream, output_stream, save_format, pattern, replacement, options) {#bytesio_bytesio_saveformat_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




### Returns

The number of replacements made.


## replace_regex(input_stream, output_stream, save_format, pattern, replacement) {#bytesio_bytesio_saveformat_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




### Returns

The number of replacements made.


## replace_regex(input_stream, output_stream, save_options, pattern, replacement, options) {#bytesio_bytesio_saveoptions_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




### Returns

The number of replacements made.


## replace_regex(input_stream, output_stream, save_options, pattern, replacement) {#bytesio_bytesio_saveoptions_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input stream using a regular expression, with the specified save format and additional options.


```python
def replace_regex(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input stream. |
| output_stream | io.BytesIO | The output stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| pattern | str | A regular expression pattern used to find matches. |
| replacement | str | A string to replace all occurrences of pattern. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




### Returns

The number of replacements made.


## See Also

* module [aspose.words.lowcode](../../)
* class [Replacer](../)

