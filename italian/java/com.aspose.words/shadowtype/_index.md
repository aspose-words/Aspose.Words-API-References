---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di ombra di una forma in Java."
type: docs
weight: 611
url: /it/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Specifica il tipo di ombra di una forma.

 **Remarks:** 

ShadowType non è un semplice attributo, ma un preset che imposta contemporaneamente diversi attributi che costituiscono l'aspetto dell'ombra.

 **Examples:** 

Mostra come lavorare con la formattazione dell'ombra per la forma.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | Primo tipo di ombra. |
| [SHADOW_10](#SHADOW-10) | Decimo tipo di ombra. |
| [SHADOW_11](#SHADOW-11) | Undicesimo tipo di ombra. |
| [SHADOW_12](#SHADOW-12) | Dodicesimo tipo di ombra. |
| [SHADOW_13](#SHADOW-13) | Tredicesimo tipo di ombra. |
| [SHADOW_14](#SHADOW-14) | Quattordicesimo tipo di ombra. |
| [SHADOW_15](#SHADOW-15) | Quindicesimo tipo di ombra. |
| [SHADOW_16](#SHADOW-16) | Sedicesimo tipo di ombra. |
| [SHADOW_17](#SHADOW-17) | Diciassettesimo tipo di ombra. |
| [SHADOW_18](#SHADOW-18) | Diciottesimo tipo di ombra. |
| [SHADOW_19](#SHADOW-19) | Diciannovesimo tipo di ombra. |
| [SHADOW_2](#SHADOW-2) | Secondo tipo di ombra. |
| [SHADOW_20](#SHADOW-20) | Ventesimo tipo di ombra. |
| [SHADOW_21](#SHADOW-21) | Ventunesimo tipo di ombra. |
| [SHADOW_22](#SHADOW-22) | Ventiduesimo tipo di ombra. |
| [SHADOW_23](#SHADOW-23) | Ventitreesimo tipo di ombra. |
| [SHADOW_24](#SHADOW-24) | Ventiquattresimo tipo di ombra. |
| [SHADOW_25](#SHADOW-25) | Venticinquesimo tipo di ombra. |
| [SHADOW_26](#SHADOW-26) | Ventiseiesimo tipo di ombra. |
| [SHADOW_27](#SHADOW-27) | Ventisettesimo tipo di ombra. |
| [SHADOW_28](#SHADOW-28) | Ventottesimo tipo di ombra. |
| [SHADOW_29](#SHADOW-29) | Ventinovesimo tipo di ombra. |
| [SHADOW_3](#SHADOW-3) | Terzo tipo di ombra. |
| [SHADOW_30](#SHADOW-30) | Trentesimo tipo di ombra. |
| [SHADOW_31](#SHADOW-31) | Trentunesimo tipo di ombra. |
| [SHADOW_32](#SHADOW-32) | Trentaduesimo tipo di ombra. |
| [SHADOW_33](#SHADOW-33) | Trentatresimo tipo di ombra. |
| [SHADOW_34](#SHADOW-34) | Tipo di ombra trentquattresimo. |
| [SHADOW_35](#SHADOW-35) | Tipo di ombra trentacinquesimo. |
| [SHADOW_36](#SHADOW-36) | Tipo di ombra trentaseiesimo. |
| [SHADOW_37](#SHADOW-37) | Tipo di ombra trentasettesimo. |
| [SHADOW_38](#SHADOW-38) | Tipo di ombra trentottesimo. |
| [SHADOW_39](#SHADOW-39) | Tipo di ombra trentanovesimo. |
| [SHADOW_4](#SHADOW-4) | Tipo di ombra quarto. |
| [SHADOW_40](#SHADOW-40) | Tipo di ombra quarantesimo. |
| [SHADOW_41](#SHADOW-41) | Tipo di ombra quarantunesimo. |
| [SHADOW_42](#SHADOW-42) | Tipo di ombra quarantaduesimo. |
| [SHADOW_43](#SHADOW-43) | Tipo di ombra quarantatresimo. |
| [SHADOW_5](#SHADOW-5) | Tipo di ombra quinto. |
| [SHADOW_6](#SHADOW-6) | Tipo di ombra sesto. |
| [SHADOW_7](#SHADOW-7) | Tipo di ombra settimo. |
| [SHADOW_8](#SHADOW-8) | Tipo di ombra ottavo. |
| [SHADOW_9](#SHADOW-9) | Tipo di ombra nono. |
| [SHADOW_MIXED](#SHADOW-MIXED) | Nessuna delle preimpostazioni di ombra predefinite. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


Primo tipo di ombra.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Decimo tipo di ombra.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


Undicesimo tipo di ombra.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


Dodicesimo tipo di ombra.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


Tredicesimo tipo di ombra.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


Quattordicesimo tipo di ombra.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


Quindicesimo tipo di ombra.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


Sedicesimo tipo di ombra.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


Diciassettesimo tipo di ombra.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


Diciottesimo tipo di ombra.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


Diciannovesimo tipo di ombra.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


Secondo tipo di ombra.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Ventesimo tipo di ombra.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Ventunesimo tipo di ombra.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Ventiduesimo tipo di ombra.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Ventitreesimo tipo di ombra.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Ventiquattresimo tipo di ombra.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Venticinquesimo tipo di ombra.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Ventiseiesimo tipo di ombra.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Ventisettesimo tipo di ombra.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Ventottesimo tipo di ombra.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Ventinovesimo tipo di ombra.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Terzo tipo di ombra.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Trentesimo tipo di ombra.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Trentunesimo tipo di ombra.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Trentaduesimo tipo di ombra.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Trentatresimo tipo di ombra.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Tipo di ombra trentquattresimo.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Tipo di ombra trentacinquesimo.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Tipo di ombra trentaseiesimo.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Tipo di ombra trentasettesimo.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Tipo di ombra trentottesimo.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Tipo di ombra trentanovesimo.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Tipo di ombra quarto.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Tipo di ombra quarantesimo.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Tipo di ombra quarantunesimo.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Tipo di ombra quarantaduesimo.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Tipo di ombra quarantatresimo.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Tipo di ombra quinto.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Tipo di ombra sesto.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Tipo di ombra settimo.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Tipo di ombra ottavo.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Tipo di ombra nono.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


Nessuna delle preimpostazioni di ombra predefinite.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
