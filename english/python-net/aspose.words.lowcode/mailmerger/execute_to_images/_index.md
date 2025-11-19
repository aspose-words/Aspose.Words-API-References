---
title: MailMerger.execute_to_images method
linktitle: execute_to_images method
articleTitle: execute_to_images method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.MailMerger.execute_to_images method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/mailmerger/execute_to_images/
---

## execute_to_images(input_file_name, save_options, field_names, field_values) {#str_imagesaveoptions_strlist_objectlist}

Performs a mail merge operation for a single record and renders the result to images.


```python
def execute_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

## execute_to_images(input_file_name, save_options, field_names, field_values, mail_merge_options) {#str_imagesaveoptions_strlist_objectlist_mailmergeoptions}

Performs a mail merge operation for a single record and renders the result to images.


```python
def execute_to_images(self, input_file_name: str, save_options: aspose.words.saving.ImageSaveOptions, field_names: List[str], field_values: List[object], mail_merge_options: aspose.words.lowcode.MailMergeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mail_merge_options | [MailMergeOptions](../../mailmergeoptions/) | Mail merge options. |

## execute_to_images(input_stream, save_options, field_names, field_values) {#bytesio_imagesaveoptions_strlist_objectlist}

Performs a mail merge operation for a single record and renders the result to images.


```python
def execute_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, field_names: List[str], field_values: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |

## execute_to_images(input_stream, save_options, field_names, field_values, mail_merge_options) {#bytesio_imagesaveoptions_strlist_objectlist_mailmergeoptions}

Performs a mail merge operation for a single record and renders the result to images.


```python
def execute_to_images(self, input_stream: io.BytesIO, save_options: aspose.words.saving.ImageSaveOptions, field_names: List[str], field_values: List[object], mail_merge_options: aspose.words.lowcode.MailMergeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's save options. |
| field_names | List[str] | Array of merge field names. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |
| field_values | List[object] | Array of values to be inserted into the merge fields. Number of elements in this array must be the same as the number of elements in fieldNames. |
| mail_merge_options | [MailMergeOptions](../../mailmergeoptions/) | Mail merge options. |

## Examples

Shows how to do mail merge operation for a single record and save result to images.

```python
# There is a several ways to do mail merge operation:
doc = MY_DIR + 'Mail merge.doc'
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
images = aw.lowcode.MailMerger.execute_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), field_names=field_names, field_values=field_values)
mail_merge_options = aw.lowcode.MailMergeOptions()
mail_merge_options.trim_whitespaces = True
images = aw.lowcode.MailMerger.execute_to_images(input_file_name=doc, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), field_names=field_names, field_values=field_values, mail_merge_options=mail_merge_options)
```

Shows how to do mail merge operation for a single record from the stream and save result to images.

```python
# There is a several ways to do mail merge operation using documents from the stream:
field_names = ['FirstName', 'Location', 'SpecialCharsInName()']
field_values = ['James Bond', 'London', 'Classified']
with system_helper.io.FileStream(MY_DIR + 'Mail merge.doc', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    images = aw.lowcode.MailMerger.execute_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), field_names=field_names, field_values=field_values)
    mail_merge_options = aw.lowcode.MailMergeOptions()
    mail_merge_options.trim_whitespaces = True
    images = aw.lowcode.MailMerger.execute_to_images(input_stream=stream_in, save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), field_names=field_names, field_values=field_values, mail_merge_options=mail_merge_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [MailMerger](../)

