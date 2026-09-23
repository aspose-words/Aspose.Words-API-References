---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines Formschattens in Java an."
type: docs
weight: 611
url: /de/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Gibt den Typ eines Formschattens an.

 **Remarks:** 

ShadowType ist kein einfaches Attribut, sondern eine Voreinstellung, die auf einmal mehrere Attribute setzt, die das Schattenaussehen bilden.

 **Examples:** 

Zeigt, wie man mit einer Schattenformatierung für die Form arbeitet.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | Erster Schatten-Typ. |
| [SHADOW_10](#SHADOW-10) | Zehnter Schatten-Typ. |
| [SHADOW_11](#SHADOW-11) | Elfter Schatten-Typ. |
| [SHADOW_12](#SHADOW-12) | Zwölfter Schattentyp. |
| [SHADOW_13](#SHADOW-13) | Dreizehnter Schattentyp. |
| [SHADOW_14](#SHADOW-14) | Vierzehnter Schattentyp. |
| [SHADOW_15](#SHADOW-15) | Fünfzehnter Schattentyp. |
| [SHADOW_16](#SHADOW-16) | Sechzehnter Schattentyp. |
| [SHADOW_17](#SHADOW-17) | Siebzehnter Schattentyp. |
| [SHADOW_18](#SHADOW-18) | Achtzehnter Schattentyp. |
| [SHADOW_19](#SHADOW-19) | Neunzehnter Schattentyp. |
| [SHADOW_2](#SHADOW-2) | Zweiter Schattentyp. |
| [SHADOW_20](#SHADOW-20) | Zwanzigster Schattentyp. |
| [SHADOW_21](#SHADOW-21) | Einundzwanzigster Schattentyp. |
| [SHADOW_22](#SHADOW-22) | Zweiundzwanzigster Schattentyp. |
| [SHADOW_23](#SHADOW-23) | Dreiundzwanzigster Schattentyp. |
| [SHADOW_24](#SHADOW-24) | Vierundzwanzigster Schattentyp. |
| [SHADOW_25](#SHADOW-25) | Fünfundzwanzigster Schattentyp. |
| [SHADOW_26](#SHADOW-26) | Sechsundzwanzigster Schattentyp. |
| [SHADOW_27](#SHADOW-27) | Siebenundzwanzigster Schattentyp. |
| [SHADOW_28](#SHADOW-28) | Achtundzwanzigster Schattentyp. |
| [SHADOW_29](#SHADOW-29) | Neunundzwanzigster Schattentyp. |
| [SHADOW_3](#SHADOW-3) | Dritter Schattentyp. |
| [SHADOW_30](#SHADOW-30) | Dreißigster Schattentyp. |
| [SHADOW_31](#SHADOW-31) | Einunddreißigster Schattentyp. |
| [SHADOW_32](#SHADOW-32) | Zweiunddreißigster Schattentyp. |
| [SHADOW_33](#SHADOW-33) | Dreiunddreißigster Schattentyp. |
| [SHADOW_34](#SHADOW-34) | Vierunddreißigster Schattentyp. |
| [SHADOW_35](#SHADOW-35) | Fünfunddreißigster Schatten-Typ. |
| [SHADOW_36](#SHADOW-36) | Sechsunddreißigster Schatten-Typ. |
| [SHADOW_37](#SHADOW-37) | Siebenunddreißigster Schatten-Typ. |
| [SHADOW_38](#SHADOW-38) | Achtunddreißigster Schatten-Typ. |
| [SHADOW_39](#SHADOW-39) | Neununddreißigster Schatten-Typ. |
| [SHADOW_4](#SHADOW-4) | Vierter Schatten-Typ. |
| [SHADOW_40](#SHADOW-40) | Vierzigster Schatten-Typ. |
| [SHADOW_41](#SHADOW-41) | Einundvierzigster Schatten-Typ. |
| [SHADOW_42](#SHADOW-42) | Zweiundvierzigster Schatten-Typ. |
| [SHADOW_43](#SHADOW-43) | Dreiundvierzigster Schatten-Typ. |
| [SHADOW_5](#SHADOW-5) | Fünfter Schatten-Typ. |
| [SHADOW_6](#SHADOW-6) | Sechster Schatten-Typ. |
| [SHADOW_7](#SHADOW-7) | Siebter Schatten-Typ. |
| [SHADOW_8](#SHADOW-8) | Achter Schatten-Typ. |
| [SHADOW_9](#SHADOW-9) | Neunter Schatten-Typ. |
| [SHADOW_MIXED](#SHADOW-MIXED) | Keine der vordefinierten Schatten-Voreinstellungen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


Erster Schatten-Typ.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Zehnter Schatten-Typ.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


Elfter Schatten-Typ.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


Zwölfter Schattentyp.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


Dreizehnter Schattentyp.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


Vierzehnter Schattentyp.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


Fünfzehnter Schattentyp.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


Sechzehnter Schattentyp.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


Siebzehnter Schattentyp.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


Achtzehnter Schattentyp.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


Neunzehnter Schattentyp.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


Zweiter Schattentyp.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Zwanzigster Schattentyp.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Einundzwanzigster Schattentyp.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Zweiundzwanzigster Schattentyp.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Dreiundzwanzigster Schattentyp.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Vierundzwanzigster Schattentyp.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Fünfundzwanzigster Schattentyp.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Sechsundzwanzigster Schattentyp.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Siebenundzwanzigster Schattentyp.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Achtundzwanzigster Schattentyp.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Neunundzwanzigster Schattentyp.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Dritter Schattentyp.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Dreißigster Schattentyp.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Einunddreißigster Schattentyp.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Zweiunddreißigster Schattentyp.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Dreiunddreißigster Schattentyp.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Vierunddreißigster Schattentyp.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Fünfunddreißigster Schatten-Typ.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Sechsunddreißigster Schatten-Typ.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Siebenunddreißigster Schatten-Typ.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Achtunddreißigster Schatten-Typ.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Neununddreißigster Schatten-Typ.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Vierter Schatten-Typ.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Vierzigster Schatten-Typ.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Einundvierzigster Schatten-Typ.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Zweiundvierzigster Schatten-Typ.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Dreiundvierzigster Schatten-Typ.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Fünfter Schatten-Typ.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Sechster Schatten-Typ.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Siebter Schatten-Typ.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Achter Schatten-Typ.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Neunter Schatten-Typ.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


Keine der vordefinierten Schatten-Voreinstellungen.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shadowType) {#toString-int}
```
public static String toString(int shadowType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
