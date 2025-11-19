---
title: Replacer.replace_to_images method
linktitle: replace_to_images method
articleTitle: replace_to_images method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Replacer.replace_to_images method"
type: docs
weight: 40
url: /python-net/aspose.words.lowcode/replacer/replace_to_images/
---

## replace_to_images(input_file_name, save_options, pattern, replacement) {#str_imagesaveoptions_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file.
Renders output to images.


```python
def replace_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |

## replace_to_images(input_file_name, save_options, pattern, replacement, options) {#str_imagesaveoptions_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file.
Renders output to images.


```python
def replace_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

## replace_to_images(input_stream, save_options, pattern, replacement) {#bytesio_imagesaveoptions_str_str}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file.
Renders output to images.


```python
def replace_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |

## replace_to_images(input_stream, save_options, pattern, replacement, options) {#bytesio_imagesaveoptions_str_str_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file.
Renders output to images.


```python
def replace_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The save options. |
| pattern | str | A string to be replaced. |
| replacement | str | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

## Examples

Shows how to replace string in the document and save result to images.

```python
# There is a several ways to replace string in the document:
doc = MY_DIR + 'Footer.docx'
pattern = '(C)2006 Aspose Pty Ltd.'
replacement = 'Copyright (C) 2024 by Aspose Pty Ltd.'
images = aw.lowcode.Replacer.replace_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), pattern=pattern, replacement=replacement)
options = aw.replacing.FindReplaceOptions()
options.find_whole_words_only = False
images = aw.lowcode.Replacer.replace_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), pattern=pattern, replacement=replacement, options=options)
```

Shows how to replace string in the document using documents from the stream and save result to images.

```python
# There is a several ways to replace string in the document using documents from the stream:
pattern = '(C)2006 Aspose Pty Ltd.'
replacement = 'Copyright (C) 2024 by Aspose Pty Ltd.'
with system_helper.io.FileStream(MY_DIR + 'Footer.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    images = aw.lowcode.Replacer.replace_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), pattern=pattern, replacement=replacement)
    options = aw.replacing.FindReplaceOptions()
    options.find_whole_words_only = False
    images = aw.lowcode.Replacer.replace_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), pattern=pattern, replacement=replacement, options=options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Replacer](../)

