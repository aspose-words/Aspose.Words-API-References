---
title: XmlDataSource class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to data of an XML file or stream to be used within a report."
type: docs
weight: 100
url: /python-net/aspose.words.reporting/xmldatasource/
---

## XmlDataSource class

Provides access to data of an XML file or stream to be used within a report.


To access data of the corresponding file or stream while generating a report, pass an instance of this class as
a data source to one of [ReportingEngine](../reportingengine/).BuildReport overloads.


In template documents, if a top-level XML element contains only a list of elements of the same type, 
an [XmlDataSource](./) instance should be treated in the same way as if it was 
a System.Data.DataTable 
instance. Otherwise, an [XmlDataSource](./) instance should be treated in the same way as if it was 
a System.Data.DataRow
instance. For more information, see template syntax reference 
(https://docs.aspose.com/display/wordsnet/Template+Syntax).


When XML Schema Definition is passed to a constructor of this class, data types of values of simple XML elements 
and attributes are determined according to the schema. So in template documents, you can work with typed values 
rather than just strings.

When XML Schema Definition is not passed to a constructor of this class, data types of values of simple XML elements 
and attributes are determined automatically upon their string representations. So in template documents, you can work 
with typed values in this case as well. The engine is capable to automatically recognize values of the following types:


* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.String
  
  
Note that for automatic recognition of data types to work, string representations of values of simple XML elements 
and attributes should be formed using invariant culture settings.

To override default behavior of XML data loading, initialize and pass a [XmlDataLoadOptions](../xmldataloadoptions/)
instance to a constructor of this class.





### Constructors
| Name | Description |
| --- | --- |
| [XmlDataSource(xml_path)](./__init__/#str) | Creates a new data source with data from an XML file using default options for XML data loading. |
| [XmlDataSource(xml_stream)](./__init__/#bytesio) | Creates a new data source with data from an XML stream using default options for XML data loading. |
| [XmlDataSource(xml_path, xml_schema_path)](./__init__/#str_str) | Creates a new data source with data from an XML file using an XML Schema Definition file. Default options are used for XML data loading. |
| [XmlDataSource(xml_stream, xml_schema_stream)](./__init__/#bytesio_bytesio) | Creates a new data source with data from an XML stream using an XML Schema Definition stream. Default options are used for XML data loading. |
| [XmlDataSource(xml_path, options)](./__init__/#str_xmldataloadoptions) | Creates a new data source with data from an XML file using the specified options for XML data loading. |
| [XmlDataSource(xml_stream, options)](./__init__/#bytesio_xmldataloadoptions) | Creates a new data source with data from an XML stream using the specified options for XML data loading. |
| [XmlDataSource(xml_path, xml_schema_path, options)](./__init__/#str_str_xmldataloadoptions) | Creates a new data source with data from an XML file using an XML Schema Definition file. The specified options are used for XML data loading. |
| [XmlDataSource(xml_stream, xml_schema_stream, options)](./__init__/#bytesio_bytesio_xmldataloadoptions) | Creates a new data source with data from an XML stream using an XML Schema Definition stream. The specified options are used for XML data loading. |

### See Also

* module [aspose.words.reporting](../)

