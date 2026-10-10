---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie un mode d'analyse des valeurs simples JSON null, booléen, nombre, entier et chaîne lors du chargement du JSON en Java."
type: docs
weight: 410
url: /fr/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Spécifie un mode d'analyse des valeurs simples JSON (null, booléen, nombre, entier et chaîne) lors du chargement du JSON. Un tel mode n'affecte pas l'analyse des valeurs de date‑heure.

 **Examples:** 

Montre comment utiliser JSON comme source de données (chaîne).

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
## Champs

| Champ | Description |
| --- | --- |
| [LOOSE](#LOOSE) | Spécifie le mode où les types des valeurs simples JSON sont déterminés lors de l'analyse de leurs représentations sous forme de chaîne. |
| [STRICT](#STRICT) | Spécifie le mode où les types des valeurs simples JSON sont déterminés à partir de la notation JSON elle‑même. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Spécifie le mode où les types des valeurs simples JSON sont déterminés lors de l'analyse de leurs représentations sous forme de chaîne. Par exemple, le type de 'prop' dans l'extrait JSON '\{ prop: "123" \}' est déterminé comme entier dans ce mode.

### STRICT {#STRICT}
```
public static int STRICT
```


Spécifie le mode où les types des valeurs simples JSON sont déterminés à partir de la notation JSON elle‑même. Par exemple, le type de 'prop' dans l'extrait JSON '\{ prop: "123" \}' est déterminé comme chaîne dans ce mode.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
