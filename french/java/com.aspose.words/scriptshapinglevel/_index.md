---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words pour Java"
description: "Décrit les niveaux de mise en forme requis par un script en Java."
type: docs
weight: 598
url: /fr/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Décrit les niveaux de mise en forme requis par un script.
## Champs

| Champ | Description |
| --- | --- |
| [FULL](#FULL) | Le script nécessite une prise en charge complète de la mise en forme. |
| [MINIMUM](#MINIMUM) | Le script nécessite une prise en charge minimale de la mise en forme. |
| [NONE](#NONE) | Le script ne nécessite pas de mise en forme. |
| [UNKNOWN](#UNKNOWN) | Ceci est utilisé lorsque le niveau du script n'est pas spécifié. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


Le script nécessite une prise en charge complète de la mise en forme.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Le script nécessite une prise en charge minimale de la mise en forme.

 **Remarks:** 

Il n'est pas clair ce que signifie Minimum. Minimum est défini pour certains scripts très populaires (Latin, Cyrillique...).

### NONE {#NONE}
```
public static int NONE
```


Le script ne nécessite pas de mise en forme.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Ceci est utilisé lorsque le niveau du script n'est pas spécifié.

 **Remarks:** 

Cela ne devrait pas se produire.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
