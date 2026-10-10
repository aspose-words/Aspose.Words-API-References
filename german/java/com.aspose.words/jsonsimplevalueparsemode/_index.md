---
title: "JsonSimpleValueParseMode"
linktitle: "JsonSimpleValueParseMode"
second_title: "Aspose.Words für Java"
description: "Gibt einen Modus zum Parsen einfacher JSON-Werte null, boolean, number, integer und string beim Laden von JSON in Java an."
type: docs
weight: 410
url: /de/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Gibt einen Modus zum Parsen einfacher JSON-Werte (null, boolean, number, integer und string) beim Laden von JSON an. Ein solcher Modus beeinflusst das Parsen von Datums‑ und Zeitwerten nicht.

 **Examples:** 

Zeigt, wie man JSON als Datenquelle (String) verwendet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [LOOSE](#LOOSE) | Gibt den Modus an, bei dem die Typen einfacher JSON‑Werte beim Parsen ihrer String‑Darstellungen ermittelt werden. |
| [STRICT](#STRICT) | Gibt den Modus an, bei dem die Typen einfacher JSON‑Werte aus der JSON‑Notation selbst ermittelt werden. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Gibt den Modus an, bei dem die Typen einfacher JSON‑Werte beim Parsen ihrer String‑Darstellungen ermittelt werden. Zum Beispiel wird der Typ von 'prop' aus dem JSON‑Snippet '\{ prop: "123" \}' in diesem Modus als Integer bestimmt.

### STRICT {#STRICT}
```
public static int STRICT
```


Gibt den Modus an, bei dem die Typen einfacher JSON‑Werte aus der JSON‑Notation selbst ermittelt werden. Zum Beispiel wird der Typ von 'prop' aus dem JSON‑Snippet '\{ prop: "123" \}' in diesem Modus als String bestimmt.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
