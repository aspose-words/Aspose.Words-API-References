---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words für Java"
description: "Beschreibt die von einem Skript in Java benötigten Shaping‑Ebenen."
type: docs
weight: 598
url: /de/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Beschreibt die vom Skript benötigten Shaping‑Ebenen.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FULL](#FULL) | Das Skript erfordert vollständige Shaping‑Unterstützung. |
| [MINIMUM](#MINIMUM) | Das Skript erfordert minimale Shaping‑Unterstützung. |
| [NONE](#NONE) | Das Skript erfordert kein Shaping. |
| [UNKNOWN](#UNKNOWN) | Dies wird verwendet, wenn die Ebene für das Skript nicht angegeben ist. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


Das Skript erfordert vollständige Shaping‑Unterstützung.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Das Skript erfordert minimale Shaping‑Unterstützung.

 **Remarks:** 

Es ist nicht klar, was Minimum bedeutet. Minimum wird für einige sehr beliebte Skripte (Lateinisch, Kyrillisch ...) festgelegt.

### NONE {#NONE}
```
public static int NONE
```


Das Skript erfordert kein Shaping.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Dies wird verwendet, wenn die Ebene für das Skript nicht angegeben ist.

 **Remarks:** 

Das sollte nicht passieren.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int scriptShapingLevel) {#toString-int}
```
public static String toString(int scriptShapingLevel)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
