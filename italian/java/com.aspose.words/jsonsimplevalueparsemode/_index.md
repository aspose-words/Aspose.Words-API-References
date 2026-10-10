---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words per Java"
description: "Specifica una modalità per l'analisi dei valori semplici JSON null, boolean, number, integer e string durante il caricamento di JSON in Java."
type: docs
weight: 410
url: /it/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Specifica una modalità per l'analisi dei valori semplici JSON (null, boolean, number, integer e string) durante il caricamento di JSON. Tale modalità non influisce sull'analisi dei valori data‑ora.

 **Examples:** 

Mostra come utilizzare JSON come origine dati (stringa).

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [LOOSE](#LOOSE) | Specifica la modalità in cui i tipi dei valori semplici JSON sono determinati durante l'analisi delle loro rappresentazioni stringa. |
| [STRICT](#STRICT) | Specifica la modalità in cui i tipi dei valori semplici JSON sono determinati direttamente dalla notazione JSON. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Specifica la modalità in cui i tipi dei valori semplici JSON sono determinati durante l'analisi delle loro rappresentazioni stringa. Ad esempio, il tipo di 'prop' dallo snippet JSON '\{ prop: "123" \}' è determinato come intero in questa modalità.

### STRICT {#STRICT}
```
public static int STRICT
```


Specifica la modalità in cui i tipi dei valori semplici JSON sono determinati direttamente dalla notazione JSON. Ad esempio, il tipo di 'prop' dallo snippet JSON '\{ prop: "123" \}' è determinato come stringa in questa modalità.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
