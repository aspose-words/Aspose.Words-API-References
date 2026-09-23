---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words per Java"
description: "Descrive i livelli di formattazione richiesti da uno script in Java."
type: docs
weight: 598
url: /it/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Descrive i livelli di shaping richiesti da uno script.
## Campi

| Campo | Descrizione |
| --- | --- |
| [FULL](#FULL) | Lo script richiede il supporto completo alla formattazione. |
| [MINIMUM](#MINIMUM) | Lo script richiede il supporto minimo alla formattazione. |
| [NONE](#NONE) | Lo script non richiede la formattazione. |
| [UNKNOWN](#UNKNOWN) | Questo è usato quando il livello per lo script non è specificato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


Lo script richiede il supporto completo alla formattazione.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Lo script richiede il supporto minimo alla formattazione.

 **Remarks:** 

Non è chiaro cosa significhi Minimum. Minimum è impostato per alcuni script molto popolari (Latino, Cirillico...).

### NONE {#NONE}
```
public static int NONE
```


Lo script non richiede la formattazione.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Questo è usato quando il livello per lo script non è specificato.

 **Remarks:** 

Non dovrebbe accadere.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
