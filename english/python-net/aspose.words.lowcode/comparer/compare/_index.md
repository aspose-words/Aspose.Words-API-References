---
title: Comparer.compare method
linktitle: compare method
articleTitle: compare method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Comparer.compare method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/comparer/compare/
---

## compare(v1, v2, output_file_name, author, date_time) {#str_str_str_str_datetime}

Compares the document with another document producing changes as number of edit and format revisions.


```python
def compare(self, v1: str, v2: str, output_file_name: str, author: str, date_time: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | str | The original document. |
| v2 | str | The modified document. |
| output_file_name | str | The output file name. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |

## compare(v1, v2, output_file_name, save_format, author, date_time) {#str_str_str_saveformat_str_datetime}

Compares the document with another document producing changes as number of edit and format revisions.


```python
def compare(self, v1: str, v2: str, output_file_name: str, save_format: aspose.words.SaveFormat, author: str, date_time: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | str | The original document. |
| v2 | str | The modified document. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |

## compare(v1, v2, output_file_name, author, date_time, compare_options) {#str_str_str_str_datetime_compareoptions}

Compares the document with another document producing changes as number of edit and format revisions.


```python
def compare(self, v1: str, v2: str, output_file_name: str, author: str, date_time: datetime.datetime, compare_options: aspose.words.comparing.CompareOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | str | The original document. |
| v2 | str | The modified document. |
| output_file_name | str | The output file name. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |
| compare_options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) | Document comparison options. |

## compare(v1, v2, output_file_name, save_format, author, date_time, compare_options) {#str_str_str_saveformat_str_datetime_compareoptions}

Compares the document with another document producing changes as number of edit and format revisions.


```python
def compare(self, v1: str, v2: str, output_file_name: str, save_format: aspose.words.SaveFormat, author: str, date_time: datetime.datetime, compare_options: aspose.words.comparing.CompareOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | str | The original document. |
| v2 | str | The modified document. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |
| compare_options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) | Document comparison options. |

## compare(v1, v2, output_stream, save_format, author, date_time) {#bytesio_bytesio_bytesio_saveformat_str_datetime}

Compares the document with another document producing changes as number of edit and format revisions.


```python
def compare(self, v1: io.BytesIO, v2: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, author: str, date_time: datetime.datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | io.BytesIO | The original document. |
| v2 | io.BytesIO | The modified document. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |

## compare(v1, v2, output_stream, save_format, author, date_time, compare_options) {#bytesio_bytesio_bytesio_saveformat_str_datetime_compareoptions}

Compares the document with another document producing changes as number of edit and format revisions.


```python
def compare(self, v1: io.BytesIO, v2: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, author: str, date_time: datetime.datetime, compare_options: aspose.words.comparing.CompareOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | io.BytesIO | The original document. |
| v2 | io.BytesIO | The modified document. |
| output_stream | io.BytesIO | The output stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| author | str | Initials of the author to use for revisions. |
| date_time | datetime.datetime | The date and time to use for revisions. |
| compare_options | [CompareOptions](../../../aspose.words.comparing/compareoptions/) | Document comparison options. |

## Examples

Shows how to simple compare documents.

```python
# There is a several ways to compare documents:
first_doc = MY_DIR + 'Table column bookmarks.docx'
second_doc = MY_DIR + 'Table column bookmarks.doc'
aw.lowcode.Comparer.compare(v1=first_doc, v2=second_doc, output_file_name=ARTIFACTS_DIR + 'LowCode.CompareDocuments.1.docx', author='Author', date_time=datetime.datetime(1, 1, 1))
aw.lowcode.Comparer.compare(v1=first_doc, v2=second_doc, output_file_name=ARTIFACTS_DIR + 'LowCode.CompareDocuments.2.docx', save_format=aw.SaveFormat.DOCX, author='Author', date_time=datetime.datetime(1, 1, 1))
compare_options = aw.comparing.CompareOptions()
compare_options.ignore_case_changes = True
aw.lowcode.Comparer.compare(v1=first_doc, v2=second_doc, output_file_name=ARTIFACTS_DIR + 'LowCode.CompareDocuments.3.docx', author='Author', date_time=datetime.datetime(1, 1, 1), compare_options=compare_options)
aw.lowcode.Comparer.compare(v1=first_doc, v2=second_doc, output_file_name=ARTIFACTS_DIR + 'LowCode.CompareDocuments.4.docx', save_format=aw.SaveFormat.DOCX, author='Author', date_time=datetime.datetime(1, 1, 1), compare_options=compare_options)
```

Shows how to compare documents from the stream.

```python
# There is a several ways to compare documents from the stream:
with system_helper.io.FileStream(MY_DIR + 'Table column bookmarks.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as first_stream_in:
    with system_helper.io.FileStream(MY_DIR + 'Table column bookmarks.doc', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as second_stream_in:
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.CompareStreamDocuments.1.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            aw.lowcode.Comparer.compare(v1=first_stream_in, v2=second_stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, author='Author', date_time=datetime.datetime(1, 1, 1))
        with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.CompareStreamDocuments.2.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
            compare_options = aw.comparing.CompareOptions()
            compare_options.ignore_case_changes = True
            aw.lowcode.Comparer.compare(v1=first_stream_in, v2=second_stream_in, output_stream=stream_out, save_format=aw.SaveFormat.DOCX, author='Author', date_time=datetime.datetime(1, 1, 1), compare_options=compare_options)
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Comparer](../)

