---
title: Merger.merge method
linktitle: merge method
articleTitle: merge method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Merger.merge method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/merger/merge/
---

## merge(output_file, input_files) {#str_strlist}

Merges the given input documents into a single output document using specified input and output file names.


```python
def merge(self, output_file: str, input_files: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_file | str | The output file name. |
| input_files | List[str] | The input file names. |

### Remarks

By default [MergeFormatMode.KEEP_SOURCE_FORMATTING](../../mergeformatmode/#KEEP_SOURCE_FORMATTING) is used.




## merge(output_file, input_files, save_format, merge_format_mode) {#str_strlist_saveformat_mergeformatmode}

Merges the given input documents into a single output document using specified input output file names and the final document format.


```python
def merge(self, output_file: str, input_files: List[str], save_format: aspose.words.SaveFormat, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_file | str | The output file name. |
| input_files | List[str] | The input file names. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

## merge(output_file, input_files, save_options, merge_format_mode) {#str_strlist_saveoptions_mergeformatmode}

Merges the given input documents into a single output document using specified input output file names and save options.


```python
def merge(self, output_file: str, input_files: List[str], save_options: aspose.words.saving.SaveOptions, merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_file | str | The output file name. |
| input_files | List[str] | The input file names. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The save options. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

## merge(input_files, merge_format_mode) {#strlist_mergeformatmode}

Merges the given input documents into a single document and returns [Document](../../../aspose.words/document/) instance of the final document.



```python
def merge(self, input_files: List[str], merge_format_mode: aspose.words.lowcode.MergeFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_files | List[str] | The input file names. |
| merge_format_mode | [MergeFormatMode](../../mergeformatmode/) | Specifies how to merge formatting that clashes. |

## See Also

* module [aspose.words.lowcode](../../)
* class [Merger](../)

