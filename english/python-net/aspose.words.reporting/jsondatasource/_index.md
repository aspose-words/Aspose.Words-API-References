﻿---
title: JsonDataSource class
linktitle: JsonDataSource class
articleTitle: JsonDataSource class
second_title: Aspose.Words for Python
description: "aspose.words.reporting.JsonDataSource class. Provides access to data of a JSON file or stream to be used within a report"
type: docs
weight: 40
url: /python-net/aspose.words.reporting/jsondatasource/
---

## JsonDataSource class

Provides access to data of a JSON file or stream to be used within a report.
To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/python-net/linq-reporting-engine/) documentation article.




To access data of the corresponding file or stream while generating a report, pass an instance of this class as
a data source to one of [ReportingEngine](../reportingengine/).BuildReport overloads.


In template documents, if a top-level JSON element is an array, a [JsonDataSource](./) instance should be
treated in the same way as if it was a System.Data.DataTable
instance. If a top-level JSON element 
is an object, a [JsonDataSource](./) instance should be treated in the same way as if it was 
a System.Data.DataRow
instance. For more information, see template syntax reference 
(https://docs.aspose.com/display/wordsnet/Template+Syntax).


In template documents, you can work with typed values of JSON elements. For convenience, the engine replaces the set 
of JSON simple types with the following one:


* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.String
  
  
The engine automatically recognizes values of the extra types upon their JSON representations.

To override default behavior of JSON data loading, initialize and pass a [JsonDataLoadOptions](../jsondataloadoptions/) instance
to a constructor of this class.





### Constructors
| Name | Description |
| --- | --- |
| [JsonDataSource(json_path)](./__init__/#str) | Creates a new data source with data from a JSON file using default options for parsing JSON data. |
| [JsonDataSource(json_stream)](./__init__/#bytesio) | Creates a new data source with data from a JSON stream using default options for parsing JSON data. |
| [JsonDataSource(json_path, options)](./__init__/#str_jsondataloadoptions) | Creates a new data source with data from a JSON file using the specified options for parsing JSON data. |
| [JsonDataSource(json_stream, options)](./__init__/#bytesio_jsondataloadoptions) | Creates a new data source with data from a JSON stream using the specified options for parsing JSON data. |

### See Also

* module [aspose.words.reporting](../)

