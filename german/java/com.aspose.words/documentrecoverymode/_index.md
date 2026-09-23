---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words für Java"
description: "Gibt die verfügbaren Wiederherstellungsoptionen an, wenn ein Dokument beim Laden in Java auf Fehler stößt."
type: docs
weight: 171
url: /de/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Gibt die verfügbaren Wiederherstellungsoptionen an, wenn ein Dokument beim Laden auf Fehler stößt.

 **Examples:** 

Zeigt, wie versucht wird, ein Dokument wiederherzustellen, wenn beim Laden Fehler aufgetreten sind.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [NONE](#NONE) | Es wird keine Wiederherstellung versucht. |
| [TRY_RECOVER](#TRY-RECOVER) | Versucht, das Dokument wiederherzustellen, wobei so viele Daten wie möglich erhalten bleiben. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Es wird keine Wiederherstellung versucht. Ist das Dokument ungültig, schlägt das Laden mit einem Fehler fehl.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Versucht, das Dokument wiederherzustellen, wobei so viele Daten wie möglich erhalten bleiben.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
