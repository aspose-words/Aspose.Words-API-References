---
title: ReportBuilder.build_report method
linktitle: build_report method
articleTitle: build_report method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.ReportBuilder.build_report method"
type: docs
weight: 10
url: /python-net/aspose.words.lowcode/reportbuilder/build_report/
---

## build_report(input_file_name, output_file_name, data) {#str_str_object}

Populates the template document with data from the specified source, generating a completed report.


```python
def build_report(self, input_file_name: str, output_file_name: str, data: object):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| data | object | A data source object. |

## build_report(input_file_name, output_file_name, data, report_builder_options) {#str_str_object_reportbuilderoptions}

Populates the template document with data from the specified source, generating a completed report with additional options.


```python
def build_report(self, input_file_name: str, output_file_name: str, data: object, report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| data | object | A data source object. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_file_name, output_file_name, save_format, data) {#str_str_saveformat_object}

Populates the template document with data from the specified source, generating a completed report with specified output format.


```python
def build_report(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, data: object):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |

## build_report(input_file_name, output_file_name, save_format, data, report_builder_options) {#str_str_saveformat_object_reportbuilderoptions}

Populates the template document with data from the specified source, generating a completed report with specified output format and additional options.


```python
def build_report(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, data: object, report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_stream, output_stream, save_format, data) {#bytesio_bytesio_saveformat_object}

Populates the template document with data from the specified source, generating a completed report from input and output streams.


```python
def build_report(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, data: object):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |

## build_report(input_stream, output_stream, save_format, data, report_builder_options) {#bytesio_bytesio_saveformat_object_reportbuilderoptions}

Populates the template document with data from the specified source, generating a completed report with specified output format and additional options, from input and output streams.


```python
def build_report(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, data: object, report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_file_name, output_file_name, data, data_source_name) {#str_str_object_str}

Populates the template document with data from the specified source, generating a completed report with a named data source reference.


```python
def build_report(self, input_file_name: str, output_file_name: str, data: object, data_source_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| data | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |

## build_report(input_file_name, output_file_name, data, data_source_name, report_builder_options) {#str_str_object_str_reportbuilderoptions}

Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options.


```python
def build_report(self, input_file_name: str, output_file_name: str, data: object, data_source_name: str, report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| data | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_file_name, output_file_name, save_format, data, data_source_name) {#str_str_saveformat_object_str}

Populates the template document with data from the specified source, generating a completed report with specified output format and a named data source reference.


```python
def build_report(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, data: object, data_source_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |

## build_report(input_file_name, output_file_name, save_format, data, data_source_name, report_builder_options) {#str_str_saveformat_object_str_reportbuilderoptions}

Populates the template document with data from the specified source, generating a completed report with specified output format, a named data source reference, and additional options.


```python
def build_report(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, data: object, data_source_name: str, report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_stream, output_stream, save_format, data, data_source_name) {#bytesio_bytesio_saveformat_object_str}

Populates the template document with data from the specified source, generating a completed report with a named data source reference.


```python
def build_report(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, data: object, data_source_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |

## build_report(input_stream, output_stream, save_format, data, data_source_name, report_builder_options) {#bytesio_bytesio_saveformat_object_str_reportbuilderoptions}

Populates the template document with data from the specified source, generating a completed report with a named data source reference and additional options.


```python
def build_report(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, data: object, data_source_name: str, report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_file_name, output_file_name, data, data_source_names) {#str_str_objectlist_strlist}

Populates the template document with data from multiple sources, generating a completed report from the specified input and output file names.
This overload automatically determines the save format based on the output file extension.


```python
def build_report(self, input_file_name: str, output_file_name: str, data: List[object], data_source_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| data | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |

## build_report(input_file_name, output_file_name, data, data_source_names, report_builder_options) {#str_str_objectlist_strlist_reportbuilderoptions}

Populates the template document with data from multiple sources, generating a completed report with additional options.
This overload automatically determines the save format based on the output file extension.


```python
def build_report(self, input_file_name: str, output_file_name: str, data: List[object], data_source_names: List[str], report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| data | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_file_name, output_file_name, save_format, data, data_source_names) {#str_str_saveformat_objectlist_strlist}

Populates the template document with data from multiple sources, generating a completed report with a specified output format.
This overload automatically determines the save format based on the output file extension.


```python
def build_report(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, data: List[object], data_source_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |

## build_report(input_file_name, output_file_name, save_format, data, data_source_names, report_builder_options) {#str_str_saveformat_objectlist_strlist_reportbuilderoptions}

Populates the template document with data from multiple sources, generating a completed report with a specified output format and additional options.


```python
def build_report(self, input_file_name: str, output_file_name: str, save_format: aspose.words.SaveFormat, data: List[object], data_source_names: List[str], report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_file_name | str | The input file name. |
| output_file_name | str | The output file name. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## build_report(input_stream, output_stream, save_format, data, data_source_names) {#bytesio_bytesio_saveformat_objectlist_strlist}

Populates the template document with data from multiple sources, generating a completed report from the specified input and output file streams.


```python
def build_report(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, data: List[object], data_source_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |

## build_report(input_stream, output_stream, save_format, data, data_source_names, report_builder_options) {#bytesio_bytesio_saveformat_objectlist_strlist_reportbuilderoptions}

Populates the template document with data from multiple sources, generating a completed report with specified output format and additional options from the specified input and output file streams.


```python
def build_report(self, input_stream: io.BytesIO, output_stream: io.BytesIO, save_format: aspose.words.SaveFormat, data: List[object], data_source_names: List[str], report_builder_options: aspose.words.lowcode.ReportBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| input_stream | io.BytesIO | The input file stream. |
| output_stream | io.BytesIO | The output file stream. |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The output's save format. |
| data | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |
| report_builder_options | [ReportBuilderOptions](../../reportbuilderoptions/) | Additional report build options. |

## See Also

* module [aspose.words.lowcode](../../)
* class [ReportBuilder](../)

