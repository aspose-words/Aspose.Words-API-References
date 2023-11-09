---
title: CsvDataSource constructor
linktitle: CsvDataSource constructor
articleTitle: CsvDataSource constructor
second_title: Aspose.Words for Python
description: "aspose.words.reporting.CsvDataSource constructor"
type: docs
weight: 10
url: /python-net/aspose.words.reporting/csvdatasource/__init__/
---

## CsvDataSource(csv_path) {#str}

Creates a new data source with data from a CSV file using default options for parsing CSV data.


```python
def __init__(self, csv_path: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| csv_path | str | The path to the CSV file to be used as the data source. |

## CsvDataSource(csv_path, options) {#str_csvdataloadoptions}

Creates a new data source with data from a CSV file using the specified options for parsing CSV data.


```python
def __init__(self, csv_path: str, options: aspose.words.reporting.CsvDataLoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| csv_path | str | The path to the CSV file to be used as the data source. |
| options | [CsvDataLoadOptions](../../csvdataloadoptions/) | Options for parsing the CSV data. |

## CsvDataSource(csv_stream) {#bytesio}

Creates a new data source with data from a CSV stream using default options for parsing CSV data.


```python
def __init__(self, csv_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| csv_stream | io.BytesIO | The stream of CSV data to be used as the data source. |

## CsvDataSource(csv_stream, options) {#bytesio_csvdataloadoptions}

Creates a new data source with data from a CSV stream using the specified options for parsing CSV data.


```python
def __init__(self, csv_stream: io.BytesIO, options: aspose.words.reporting.CsvDataLoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| csv_stream | io.BytesIO | The stream of CSV data to be used as the data source. |
| options | [CsvDataLoadOptions](../../csvdataloadoptions/) | Options for parsing the CSV data. |

## See Also

* module [aspose.words.reporting](../../)
* class [CsvDataSource](../)

