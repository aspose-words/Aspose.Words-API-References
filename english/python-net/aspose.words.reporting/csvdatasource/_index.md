﻿---
title: CsvDataSource class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to data of a CSV file or stream to be used within a report"
type: docs
weight: 20
url: /python-net/aspose.words.reporting/csvdatasource/
---

## CsvDataSource class

Provides access to data of a CSV file or stream to be used within a report.
To learn more, visit the [LINQ Reporting Engine](https://docs.aspose.com/words/python-net/linq-reporting-engine/) documentation article.




To access data of the corresponding file or stream while generating a report, pass an instance of this class as
a data source to one of [ReportingEngine](../reportingengine/).BuildReport overloads.


In template documents, a [CsvDataSource](./) instance should be treated in the same way as if it was
a System.Data.DataTable 
instance. For more information, see template syntax reference 
(https://docs.aspose.com/display/wordsnet/Template+Syntax).


Data types of comma-separated values are determined automatically upon their string representations. So in template
documents, you can work with typed values rather than just strings. The engine is capable to automatically recognize 
values of the following types:


* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.Nullable`1
  
  
* System.String
  
  
Note that for automatic recognition of data types to work, string representations of comma-separated values should 
be formed using invariant culture settings.

To override default behavior of CSV data loading, initialize and pass a [CsvDataLoadOptions](../csvdataloadoptions/) instance
to a constructor of this class.





### Constructors
| Name | Description |
| --- | --- |
| [CsvDataSource(csv_path)](./__init__/#str) | Creates a new data source with data from a CSV file using default options for parsing CSV data. |
| [CsvDataSource(csv_path, options)](./__init__/#str_csvdataloadoptions) | Creates a new data source with data from a CSV file using the specified options for parsing CSV data. |
| [CsvDataSource(csv_stream)](./__init__/#bytesio) | Creates a new data source with data from a CSV stream using default options for parsing CSV data. |
| [CsvDataSource(csv_stream, options)](./__init__/#bytesio_csvdataloadoptions) | Creates a new data source with data from a CSV stream using the specified options for parsing CSV data. |

### See Also

* module [aspose.words.reporting](../)

