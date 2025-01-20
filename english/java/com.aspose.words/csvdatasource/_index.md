---
title: CsvDataSource
linktitle: CsvDataSource
second_title: Aspose.Words for Java
description: Provides access to data of a CSV file or stream to be used within a report in Java.
type: docs
weight: 134
url: /java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Provides access to data of a CSV file or stream to be used within a report.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.

 **Remarks:** 

To access data of the corresponding file or stream while generating a report, pass an instance of this class as a data source to one of [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport overloads.

In template documents, a [CsvDataSource](../../com.aspose.words/csvdatasource/) instance should be treated in the same way as if it was a [DataTable](../../com.aspose.words.net.system.data/datatable/) instance. For more information, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Data types of comma-separated values are determined automatically upon their string representations. So in template documents, you can work with typed values rather than just strings. The engine is capable to automatically recognize values of the following types:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Note that for automatic recognition of data types to work, string representations of comma-separated values should be formed using invariant culture settings.

To override default behavior of CSV data loading, initialize and pass a [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) instance to a constructor of this class.

 **Examples:** 

Shows how to use CSV as a data source (string).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | Creates a new data source with data from a CSV file using default options for parsing CSV data. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | Creates a new data source with data from a CSV file using the specified options for parsing CSV data. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Initializes a new instance of this class. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Initializes a new instance of this class. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


Creates a new data source with data from a CSV file using default options for parsing CSV data.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| csvPath | java.lang.String | The path to the CSV file to be used as the data source. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Creates a new data source with data from a CSV file using the specified options for parsing CSV data.

 **Examples:** 

Shows how to use CSV as a data source (string).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| csvPath | java.lang.String | The path to the CSV file to be used as the data source. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | Options for parsing the CSV data. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

