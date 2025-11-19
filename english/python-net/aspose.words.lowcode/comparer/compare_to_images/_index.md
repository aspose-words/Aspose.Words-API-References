---
title: Comparer.compare_to_images method
linktitle: compare_to_images method
articleTitle: compare_to_images method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Comparer.compare_to_images method"
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/comparer/compare_to_images/
---

## compare_to_images(v1, v2, image_save_options, author, date_time) {#str_str_imagesaveoptions_str_datetime}

Compares two documents and saves the differences as images.
Each item in the returned array represents a single page of the output rendered as an image.


```python
def compare_to_images(self, v1: str, v2: str, image_save_options: aspose.words.saving.ImageSaveOptions, author: str, date_time: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | str | The original document. |
| v2 | str | The modified document. |
| image_save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's image save options. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |

## compare_to_images(v1, v2, image_save_options, author, date_time, compare_options) {#str_str_imagesaveoptions_str_datetime_compareoptions}

Compares two documents and saves the differences as images.
Each item in the returned array represents a single page of the output rendered as an image.


```python
def compare_to_images(self, v1: str, v2: str, image_save_options: aspose.words.saving.ImageSaveOptions, author: str, date_time: datetime.datetime, compare_options: aspose.words.comparing.CompareOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | str | The original document. |
| v2 | str | The modified document. |
| image_save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's image save options. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |
| compare_options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) | Document comparison options. |

## compare_to_images(v1, v2, image_save_options, author, date_time) {#bytesio_bytesio_imagesaveoptions_str_datetime}

Compares two documents and saves the differences as images.
Each item in the returned array represents a single page of the output rendered as an image.


```python
def compare_to_images(self, v1: io.BytesIO, v2: io.BytesIO, image_save_options: aspose.words.saving.ImageSaveOptions, author: str, date_time: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | io.BytesIO | The original document. |
| v2 | io.BytesIO | The modified document. |
| image_save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's image save options. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |

## compare_to_images(v1, v2, image_save_options, author, date_time, compare_options) {#bytesio_bytesio_imagesaveoptions_str_datetime_compareoptions}

Compares two documents and saves the differences as images.
Each item in the returned array represents a single page of the output rendered as an image.


```python
def compare_to_images(self, v1: io.BytesIO, v2: io.BytesIO, image_save_options: aspose.words.saving.ImageSaveOptions, author: str, date_time: datetime.datetime, compare_options: aspose.words.comparing.CompareOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | io.BytesIO | The original document. |
| v2 | io.BytesIO | The modified document. |
| image_save_options | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | The output's image save options. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |
| compare_options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) | Document comparison options. |

## Examples

Shows how to compare documents and save results as images.

```python
# There is a several ways to compare documents:
first_doc = MY_DIR + 'Table column bookmarks.docx'
second_doc = MY_DIR + 'Table column bookmarks.doc'
pages = aw.lowcode.Comparer.compare_to_images(v1=first_doc, v2=second_doc, image_save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), author='Author', date_time=datetime.datetime(1, 1, 1))
with system_helper.io.FileStream(first_doc, system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as first_stream_in:
    with system_helper.io.FileStream(second_doc, system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as second_stream_in:
        compare_options = aw.comparing.CompareOptions()
        compare_options.ignore_case_changes = True
        pages = aw.lowcode.Comparer.compare_to_images(v1=first_stream_in, v2=second_stream_in, image_save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG), author='Author', date_time=datetime.datetime(1, 1, 1), compare_options=compare_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Comparer](../)

