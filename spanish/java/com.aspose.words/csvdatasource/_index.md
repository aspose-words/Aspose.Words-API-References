---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso a los datos de un archivo CSV o flujo para ser utilizado dentro de un informe en Java."
type: docs
weight: 138
url: /es/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Proporciona acceso a los datos de un archivo CSV o flujo para ser utilizados dentro de un informe.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Para acceder a los datos del archivo o flujo correspondiente al generar un informe, pase una instancia de esta clase como origen de datos a una de las sobrecargas de [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport.

En los documentos de plantilla, una instancia de [CsvDataSource](../../com.aspose.words/csvdatasource/) debe tratarse de la misma manera que si fuera una instancia de [DataTable](../../com.aspose.words.net.system.data/datatable/). Para obtener más información, consulte la referencia de sintaxis de plantillas (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Los tipos de datos de los valores separados por comas se determinan automáticamente a partir de sus representaciones en cadena. Así, en los documentos de plantilla, puede trabajar con valores tipados en lugar de solo cadenas. El motor es capaz de reconocer automáticamente valores de los siguientes tipos:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Tenga en cuenta que, para que funcione el reconocimiento automático de tipos de datos, las representaciones en cadena de los valores separados por comas deben formarse utilizando configuraciones de cultura invariantes.

Para sobrescribir el comportamiento predeterminado de la carga de datos CSV, inicialice y pase una instancia de [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) al constructor de esta clase.

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones predeterminadas para analizar datos CSV. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones especificadas para analizar datos CSV. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Inicializa una nueva instancia de esta clase. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Inicializa una nueva instancia de esta clase. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones predeterminadas para analizar datos CSV.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| csvPath | java.lang.String | La ruta al archivo CSV que se utilizará como fuente de datos. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones especificadas para analizar datos CSV.

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| csvPath | java.lang.String | La ruta al archivo CSV que se utilizará como fuente de datos. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | Opciones para analizar los datos CSV. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

