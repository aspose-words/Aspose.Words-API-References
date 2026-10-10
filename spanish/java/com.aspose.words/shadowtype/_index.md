---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de sombra de una forma en Java."
type: docs
weight: 611
url: /es/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Especifica el tipo de sombra de una forma.

 **Remarks:** 

ShadowType no es un atributo simple, sino un preset que establece de una vez varios atributos que forman la apariencia de la sombra.

 **Examples:** 

Muestra cómo trabajar con el formato de sombra para la forma.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | Primer tipo de sombra. |
| [SHADOW_10](#SHADOW-10) | Décimo tipo de sombra. |
| [SHADOW_11](#SHADOW-11) | Undécimo tipo de sombra. |
| [SHADOW_12](#SHADOW-12) | Duodécimo tipo de sombra. |
| [SHADOW_13](#SHADOW-13) | Decimotercero tipo de sombra. |
| [SHADOW_14](#SHADOW-14) | Decimocuarto tipo de sombra. |
| [SHADOW_15](#SHADOW-15) | Decimoquinto tipo de sombra. |
| [SHADOW_16](#SHADOW-16) | Decimosexto tipo de sombra. |
| [SHADOW_17](#SHADOW-17) | Decimoséptimo tipo de sombra. |
| [SHADOW_18](#SHADOW-18) | Decimoctavo tipo de sombra. |
| [SHADOW_19](#SHADOW-19) | Decimonoveno tipo de sombra. |
| [SHADOW_2](#SHADOW-2) | Segundo tipo de sombra. |
| [SHADOW_20](#SHADOW-20) | Vigésimo tipo de sombra. |
| [SHADOW_21](#SHADOW-21) | Vigésimo primero tipo de sombra. |
| [SHADOW_22](#SHADOW-22) | Vigésimo segundo tipo de sombra. |
| [SHADOW_23](#SHADOW-23) | Vigésimo tercero tipo de sombra. |
| [SHADOW_24](#SHADOW-24) | Vigésimo cuarto tipo de sombra. |
| [SHADOW_25](#SHADOW-25) | Vigésimo quinto tipo de sombra. |
| [SHADOW_26](#SHADOW-26) | Vigésimo sexto tipo de sombra. |
| [SHADOW_27](#SHADOW-27) | Vigésimo séptimo tipo de sombra. |
| [SHADOW_28](#SHADOW-28) | Vigésimo octavo tipo de sombra. |
| [SHADOW_29](#SHADOW-29) | Vigésimo noveno tipo de sombra. |
| [SHADOW_3](#SHADOW-3) | Tercero tipo de sombra. |
| [SHADOW_30](#SHADOW-30) | Trigésimo tipo de sombra. |
| [SHADOW_31](#SHADOW-31) | Trigésimo primero tipo de sombra. |
| [SHADOW_32](#SHADOW-32) | Trigésimo segundo tipo de sombra. |
| [SHADOW_33](#SHADOW-33) | Trigésimo tercero tipo de sombra. |
| [SHADOW_34](#SHADOW-34) | Tipo de sombra treinta y cuatro. |
| [SHADOW_35](#SHADOW-35) | Tipo de sombra treinta y cinco. |
| [SHADOW_36](#SHADOW-36) | Tipo de sombra treinta y seis. |
| [SHADOW_37](#SHADOW-37) | Tipo de sombra treinta y siete. |
| [SHADOW_38](#SHADOW-38) | Tipo de sombra treinta y ocho. |
| [SHADOW_39](#SHADOW-39) | Tipo de sombra treinta y nueve. |
| [SHADOW_4](#SHADOW-4) | Tipo de sombra cuarto. |
| [SHADOW_40](#SHADOW-40) | Tipo de sombra cuarenta. |
| [SHADOW_41](#SHADOW-41) | Tipo de sombra cuarenta y uno. |
| [SHADOW_42](#SHADOW-42) | Tipo de sombra cuarenta y dos. |
| [SHADOW_43](#SHADOW-43) | Tipo de sombra cuarenta y tres. |
| [SHADOW_5](#SHADOW-5) | Tipo de sombra quinto. |
| [SHADOW_6](#SHADOW-6) | Tipo de sombra sexto. |
| [SHADOW_7](#SHADOW-7) | Tipo de sombra séptimo. |
| [SHADOW_8](#SHADOW-8) | Tipo de sombra octavo. |
| [SHADOW_9](#SHADOW-9) | Tipo de sombra noveno. |
| [SHADOW_MIXED](#SHADOW-MIXED) | Ninguno de los preajustes de sombra predefinidos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


Primer tipo de sombra.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Décimo tipo de sombra.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


Undécimo tipo de sombra.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


Duodécimo tipo de sombra.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


Decimotercero tipo de sombra.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


Decimocuarto tipo de sombra.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


Decimoquinto tipo de sombra.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


Decimosexto tipo de sombra.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


Decimoséptimo tipo de sombra.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


Decimoctavo tipo de sombra.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


Decimonoveno tipo de sombra.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


Segundo tipo de sombra.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Vigésimo tipo de sombra.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Vigésimo primero tipo de sombra.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Vigésimo segundo tipo de sombra.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Vigésimo tercero tipo de sombra.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Vigésimo cuarto tipo de sombra.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Vigésimo quinto tipo de sombra.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Vigésimo sexto tipo de sombra.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Vigésimo séptimo tipo de sombra.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Vigésimo octavo tipo de sombra.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Vigésimo noveno tipo de sombra.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Tercero tipo de sombra.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Trigésimo tipo de sombra.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Trigésimo primero tipo de sombra.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Trigésimo segundo tipo de sombra.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Trigésimo tercero tipo de sombra.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Tipo de sombra treinta y cuatro.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Tipo de sombra treinta y cinco.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Tipo de sombra treinta y seis.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Tipo de sombra treinta y siete.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Tipo de sombra treinta y ocho.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Tipo de sombra treinta y nueve.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Tipo de sombra cuarto.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Tipo de sombra cuarenta.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Tipo de sombra cuarenta y uno.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Tipo de sombra cuarenta y dos.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Tipo de sombra cuarenta y tres.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Tipo de sombra quinto.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Tipo de sombra sexto.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Tipo de sombra séptimo.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Tipo de sombra octavo.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Tipo de sombra noveno.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


Ninguno de los preajustes de sombra predefinidos.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
