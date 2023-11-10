---
title: XmlDataSource constructor
linktitle: XmlDataSource constructor
articleTitle: XmlDataSource constructor
second_title: Aspose.Words for Python
description: "aspose.words.reporting.XmlDataSource constructor"
type: docs
weight: 10
url: /python-net/aspose.words.reporting/xmldatasource/__init__/
---

## XmlDataSource(xml_path) {#str}

Creates a new data source with data from an XML file using default options for XML data loading.


```python
def __init__(self, xml_path: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_path | str | The path to the XML file to be used as the data source. |

## XmlDataSource(xml_stream) {#bytesio}

Creates a new data source with data from an XML stream using default options for XML data loading.


```python
def __init__(self, xml_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_stream | io.BytesIO | The stream of XML data to be used as the data source. |

## XmlDataSource(xml_path, xml_schema_path) {#str_str}

Creates a new data source with data from an XML file using an XML Schema Definition file. Default options
are used for XML data loading.


```python
def __init__(self, xml_path: str, xml_schema_path: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_path | str | The path to the XML file to be used as the data source. |
| xml_schema_path | str | The path to the XML Schema Definition file that provides schema for the XML file. |

## XmlDataSource(xml_stream, xml_schema_stream) {#bytesio_bytesio}

Creates a new data source with data from an XML stream using an XML Schema Definition stream. Default options
are used for XML data loading.


```python
def __init__(self, xml_stream: io.BytesIO, xml_schema_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_stream | io.BytesIO | The stream of XML data to be used as the data source. |
| xml_schema_stream | io.BytesIO | The stream of XML Schema Definition that provides schema for the XML data. |

## XmlDataSource(xml_path, options) {#str_xmldataloadoptions}

Creates a new data source with data from an XML file using the specified options for XML data loading.


```python
def __init__(self, xml_path: str, options: aspose.words.reporting.XmlDataLoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_path | str | The path to the XML file to be used as the data source. |
| options | [XmlDataLoadOptions](../../xmldataloadoptions/) | Options for XML data loading. |

## XmlDataSource(xml_stream, options) {#bytesio_xmldataloadoptions}

Creates a new data source with data from an XML stream using the specified options for XML data loading.


```python
def __init__(self, xml_stream: io.BytesIO, options: aspose.words.reporting.XmlDataLoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_stream | io.BytesIO | The stream of XML data to be used as the data source. |
| options | [XmlDataLoadOptions](../../xmldataloadoptions/) | Options for XML data loading. |

## XmlDataSource(xml_path, xml_schema_path, options) {#str_str_xmldataloadoptions}

Creates a new data source with data from an XML file using an XML Schema Definition file. The specified
options are used for XML data loading.


```python
def __init__(self, xml_path: str, xml_schema_path: str, options: aspose.words.reporting.XmlDataLoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_path | str | The path to the XML file to be used as the data source. |
| xml_schema_path | str | The path to the XML Schema Definition file that provides schema for the XML file. |
| options | [XmlDataLoadOptions](../../xmldataloadoptions/) | Options for XML data loading. |

## XmlDataSource(xml_stream, xml_schema_stream, options) {#bytesio_bytesio_xmldataloadoptions}

Creates a new data source with data from an XML stream using an XML Schema Definition stream. The specified
options are used for XML data loading.


```python
def __init__(self, xml_stream: io.BytesIO, xml_schema_stream: io.BytesIO, options: aspose.words.reporting.XmlDataLoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xml_stream | io.BytesIO | The stream of XML data to be used as the data source. |
| xml_schema_stream | io.BytesIO | The stream of XML Schema Definition that provides schema for the XML data. |
| options | [XmlDataLoadOptions](../../xmldataloadoptions/) | Options for XML data loading. |

## See Also

* module [aspose.words.reporting](../../)
* class [XmlDataSource](../)

