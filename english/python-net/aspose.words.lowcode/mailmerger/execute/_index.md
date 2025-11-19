---
title: MailMerger.execute method
linktitle: execute method
articleTitle: execute method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.MailMerger.execute method"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/mailmerger/execute/
---

## execute(input_file_name, output_file_name, field_names, field_values) {#str_str_strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, input_file_name: str, output_file_name: str, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




## execute(input_file_name, output_file_name, save_format, field_names, field_values) {#str_str_saveformat_strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




## execute(input_file_name, output_file_name, save_format, field_names, field_values, mail_merge_options) {#str_str_saveformat_strlist_objectlist_mailmergeoptions}

Performs a mail merge operation for a single record.


```python
def execute(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, field_names: List[str], field_values: List[object], mail_merge_options: aspose.words.lowcode.MailMergeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mail_merge_options | [MailMergeOptions](../../mailmergeoptions/) | Mail merge options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




## execute(input_file_name, output_file_name, save_options, field_names, field_values) {#str_str_saveoptions_strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




## execute(input_file_name, output_file_name, save_options, field_names, field_values, mail_merge_options) {#str_str_saveoptions_strlist_objectlist_mailmergeoptions}

Performs a mail merge operation for a single record.


```python
def execute(self, input_file_name: str, output_file_name: str, save_options: aspose.words.saving.SaveOptions, field_names: List[str], field_values: List[object], mail_merge_options: aspose.words.lowcode.MailMergeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mail_merge_options | [MailMergeOptions](../../mailmergeoptions/) | Mail merge options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.




## execute(input_stream, output_stream, save_format, field_names, field_values) {#bytesio_bytesio_saveformat_strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




## execute(input_stream, output_stream, save_format, field_names, field_values, mail_merge_options) {#bytesio_bytesio_saveformat_strlist_objectlist_mailmergeoptions}

Performs a mail merge operation for a single record.


```python
def execute(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, field_names: List[str], field_values: List[object], mail_merge_options: aspose.words.lowcode.MailMergeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mail_merge_options | [MailMergeOptions](../../mailmergeoptions/) | Mail merge options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




## execute(input_stream, output_stream, save_options, field_names, field_values) {#bytesio_bytesio_saveoptions_strlist_objectlist}

Performs a mail merge operation for a single record.


```python
def execute(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




## execute(input_stream, output_stream, save_options, field_names, field_values, mail_merge_options) {#bytesio_bytesio_saveoptions_strlist_objectlist_mailmergeoptions}

Performs a mail merge operation for a single record.


```python
def execute(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions, field_names: List[str], field_values: List[object], mail_merge_options: aspose.words.lowcode.MailMergeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mail_merge_options | [MailMergeOptions](../../mailmergeoptions/) | Mail merge options. |

### Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.




## execute() {#default}

Execute the processor action.


```python
def execute(self):
    ...
```

## Examples

Shows how to do mail merge operation for a single record.

```python
# There is a several ways to do mail merge operation:
doc = MY_DIR + 'Mail merge.doc'
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
aw.lowcode.MailMerger.execute(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.MailMerge.1.docx', field_names=field_names, field_values=field_values)
aw.lowcode.MailMerger.execute(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.MailMerge.2.docx', save_format=aw.SaveFormat.DOCX, field_names=field_names, field_values=field_values)
mail_merge_options = aw.lowcode.MailMergeOptions()
mail_merge_options.trim_whitespaces = True
aw.lowcode.MailMerger.execute(input_file_name=doc, output_file_name=ARTIFACTS_DIR + 'LowCode.MailMerge.3.docx', save_format=aw.SaveFormat.DOCX, field_names=field_names, field_values=field_values, mail_merge_options=mail_merge_options)
```

Shows how to do mail merge operation for a single record from the stream.

```python
# There is a several ways to do mail merge operation using documents from the stream:
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
with system_helper.io.FileStream(MY_DIR + 'Mail merge.doc', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MailMergeStream.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.MailMerger.execute(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, field_names=field_names, field_values=field_values)
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.MailMergeStream.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        mail_merge_options = aw.lowcode.MailMergeOptions()
        mail_merge_options.trim_whitespaces = True
        aw.lowcode.MailMerger.execute(input_stream=stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, field_names=field_names, field_values=field_values, mail_merge_options=mail_merge_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [MailMerger](../../mailmerger/)

