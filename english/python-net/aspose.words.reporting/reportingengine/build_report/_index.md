---
title: ReportingEngine.build_report method
linktitle: build_report method
articleTitle: build_report method
second_title: Aspose.Words for Python
description: "aspose.words.reporting.ReportingEngine.build_report method"
type: docs
weight: 50
url: /python-net/aspose.words.reporting/reportingengine/build_report/
---

## build_report(document, data_source) {#document_object}

Populates the specified template document with data from the specified source making it a ready report.


```python
def build_report(self, document: aspose.words.Document, data_source: object):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../../aspose.words/document/) | A template document to be populated with data. |
| data_source | object | A data source object. |

### Remarks

Using this overload you can reference the data source's members in the template document, but you cannot
reference the data source object itself. You should use the [ReportingEngine.build_report()](./#document_object_str)
overload to achieve this.


A data source object can be of one of the following types:


* [XmlDataSource](../../xmldatasource/)
  
  
* [JsonDataSource](../../jsondatasource/)
  
  
* [CsvDataSource](../../csvdatasource/)
  
  



### Returns

A flag indicating whether parsing of the template document was successful.
The returned flag makes sense only if a value of the [ReportingEngine.options](../options/) property includes
the [ReportBuildOptions.INLINE_ERROR_MESSAGES](../../reportbuildoptions/#INLINE_ERROR_MESSAGES) option.


## build_report(document, data_source, data_source_name) {#document_object_str}

Populates the specified template document with data from the specified source making it a ready report.


```python
def build_report(self, document: aspose.words.Document, data_source: object, data_source_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../../aspose.words/document/) | A template document to be populated with data. |
| data_source | object | A data source object. |
| data_source_name | str | A name to reference the data source object in the template. |

### Remarks

Using this overload you can reference the data source's members and the data source object itself in the template.
If you are not going to reference the data source object itself, you can omit *dataSourceName*
passing``None`` or use the [ReportingEngine.build_report()](./#document_object) overload.


A data source object can be of one of the following types:


* [XmlDataSource](../../xmldatasource/)
  
  
* [JsonDataSource](../../jsondatasource/)
  
  
* [CsvDataSource](../../csvdatasource/)
  
  



### Returns

A flag indicating whether parsing of the template document was successful.
The returned flag makes sense only if a value of the [ReportingEngine.options](../options/) property includes
the [ReportBuildOptions.INLINE_ERROR_MESSAGES](../../reportbuildoptions/#INLINE_ERROR_MESSAGES) option.


## build_report(document, data_sources, data_source_names) {#document_objectlist_strlist}

Populates the specified template document with data from the specified sources making it a ready report.


```python
def build_report(self, document: aspose.words.Document, data_sources: List[object], data_source_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../../aspose.words/document/) | A template document to be populated with data. |
| data_sources | List[object] | An array of data source objects. |
| data_source_names | List[str] | An array of names to reference the data source objects within the template. |

### Remarks

Using this overload you can reference multiple data source objects and their members in the template.
The name of the first data source can be omitted (i.e. be an empty string or ``None``) if you are going to
reference the data source's members but not the data source object itself. Names of the other data sources
must be specified and unique.


If you are going to use a single data source, consider using of [ReportingEngine.build_report()](./#document_object)
and [ReportingEngine.build_report()](./#document_object_str) overloads instead.


A data source object can be of one of the following types:


* [XmlDataSource](../../xmldatasource/)
  
  
* [JsonDataSource](../../jsondatasource/)
  
  
* [CsvDataSource](../../csvdatasource/)
  
  



### Returns

A flag indicating whether parsing of the template document was successful.
The returned flag makes sense only if a value of the [ReportingEngine.options](../options/) property includes
the [ReportBuildOptions.INLINE_ERROR_MESSAGES](../../reportbuildoptions/#INLINE_ERROR_MESSAGES) option.


## See Also

* module [aspose.words.reporting](../../)
* class [ReportingEngine](../)

