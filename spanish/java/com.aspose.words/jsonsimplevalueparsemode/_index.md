---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words para Java"
description: "Especifica un modo para analizar valores simples de JSON nulo, booleano, número, entero y cadena al cargar JSON en Java."
type: docs
weight: 410
url: /es/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Especifica un modo para analizar valores simples de JSON (nulo, booleano, número, entero y cadena) al cargar JSON. Este modo no afecta el análisis de valores de fecha y hora.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [LOOSE](#LOOSE) | Especifica el modo en el que los tipos de valores simples de JSON se determinan al analizar sus representaciones en cadena. |
| [STRICT](#STRICT) | Especifica el modo en el que los tipos de valores simples de JSON se determinan a partir de la notación JSON misma. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Especifica el modo en el que los tipos de valores simples de JSON se determinan al analizar sus representaciones en cadena. Por ejemplo, el tipo de 'prop' del fragmento JSON '\{ prop: "123" \}' se determina como entero en este modo.

### STRICT {#STRICT}
```
public static int STRICT
```


Especifica el modo en el que los tipos de valores simples de JSON se determinan a partir de la notación JSON misma. Por ejemplo, el tipo de 'prop' del fragmento JSON '\{ prop: "123" \}' se determina como cadena en este modo.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int jsonSimpleValueParseMode) {#toString-int}
```
public static String toString(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
