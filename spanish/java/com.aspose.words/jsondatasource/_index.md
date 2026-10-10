---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso a los datos de un archivo o flujo JSON para ser utilizados dentro de un informe en Java."
type: docs
weight: 409
url: /es/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Proporciona acceso a los datos de un archivo o flujo JSON para usar dentro de un informe.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Para acceder a los datos del archivo o flujo correspondiente al generar un informe, pase una instancia de esta clase como origen de datos a una de las sobrecargas de [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport.

En los documentos de plantilla, si un elemento JSON de nivel superior es una matriz, una instancia de [JsonDataSource](../../com.aspose.words/jsondatasource/) debe tratarse de la misma manera que si fuera una instancia de [DataTable](../../com.aspose.words.net.system.data/datatable/). Si un elemento JSON de nivel superior es un objeto, una instancia de [JsonDataSource](../../com.aspose.words/jsondatasource/) debe tratarse de la misma manera que si fuera una instancia de [DataRow](../../com.aspose.words.net.system.data/datarow/). Para obtener más información, consulte la referencia de sintaxis de plantillas (https://docs.aspose.com/display/wordsjava/Template+Syntax).

En los documentos de plantilla, puede trabajar con valores tipados de los elementos JSON. Para mayor comodidad, el motor reemplaza el conjunto de tipos simples de JSON con el siguiente:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

El motor reconoce automáticamente los valores de los tipos adicionales a partir de sus representaciones JSON.

Para sobrescribir el comportamiento predeterminado de la carga de datos JSON, inicialice y pase una instancia de [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) al constructor de esta clase.

 **Examples:** 

Muestra cómo usar JSON como origen de datos (cadena).

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | Crea un nuevo origen de datos con datos de un archivo JSON usando las opciones predeterminadas para analizar datos JSON. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Inicializa una nueva instancia de esta clase. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | Crea un nuevo origen de datos con datos de un archivo JSON usando las opciones especificadas para analizar datos JSON. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Inicializa una nueva instancia de esta clase. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


Crea un nuevo origen de datos con datos de un archivo JSON usando las opciones predeterminadas para analizar datos JSON.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonPath | java.lang.String | La ruta al archivo JSON que se utilizará como origen de datos. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Crea un nuevo origen de datos con datos de un archivo JSON usando las opciones especificadas para analizar datos JSON.

 **Examples:** 

Muestra cómo usar JSON como origen de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonPath | java.lang.String | La ruta al archivo JSON que se utilizará como origen de datos. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | Opciones para analizar datos JSON. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

