---
title: JsonDataSource
linktitle: JsonDataSource
second_title: Aspose.Words for Java
description: Provides access to data of a JSON file or stream to be used within a report in Java.
type: docs
weight: 399
url: /java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Provides access to data of a JSON file or stream to be used within a report.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.

 **Remarks:** 

To access data of the corresponding file or stream while generating a report, pass an instance of this class as a data source to one of [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport overloads.

In template documents, if a top-level JSON element is an array, a [JsonDataSource](../../com.aspose.words/jsondatasource/) instance should be treated in the same way as if it was a [DataTable](../../com.aspose.words.net.system.data/datatable/) instance. If a top-level JSON element is an object, a [JsonDataSource](../../com.aspose.words/jsondatasource/) instance should be treated in the same way as if it was a [DataRow](../../com.aspose.words.net.system.data/datarow/) instance. For more information, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

In template documents, you can work with typed values of JSON elements. For convenience, the engine replaces the set of JSON simple types with the following one:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

The engine automatically recognizes values of the extra types upon their JSON representations.

To override default behavior of JSON data loading, initialize and pass a [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) instance to a constructor of this class.

 **Examples:** 

Shows how to use JSON as a data source (string).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | Creates a new data source with data from a JSON file using default options for parsing JSON data. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Initializes a new instance of this class. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | Creates a new data source with data from a JSON file using the specified options for parsing JSON data. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Initializes a new instance of this class. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


Creates a new data source with data from a JSON file using default options for parsing JSON data.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonPath | java.lang.String | The path to the JSON file to be used as the data source. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Creates a new data source with data from a JSON file using the specified options for parsing JSON data.

 **Examples:** 

Shows how to use JSON as a data source (string).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonPath | java.lang.String | The path to the JSON file to be used as the data source. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | Options for parsing JSON data. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

