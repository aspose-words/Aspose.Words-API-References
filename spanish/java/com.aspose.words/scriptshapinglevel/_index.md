---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words para Java"
description: "Describe los niveles de conformado requeridos por un script en Java."
type: docs
weight: 598
url: /es/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Describe los niveles de conformado requeridos por un script.
## Campos

| Campo | Descripción |
| --- | --- |
| [FULL](#FULL) | El script requiere soporte completo de conformado. |
| [MINIMUM](#MINIMUM) | El script requiere soporte mínimo de conformado. |
| [NONE](#NONE) | El script no requiere conformado. |
| [UNKNOWN](#UNKNOWN) | Esto se usa cuando no se especifica el nivel para el script. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


El script requiere soporte completo de conformado.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


El script requiere soporte mínimo de conformado.

 **Remarks:** 

No está claro qué significa Minimum. Minimum se establece para algunos scripts muy populares (Latín, Cirílico...).

### NONE {#NONE}
```
public static int NONE
```


El script no requiere conformado.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Esto se usa cuando no se especifica el nivel para el script.

 **Remarks:** 

No debería suceder.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
