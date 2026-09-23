---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'ombre d'une forme en Java."
type: docs
weight: 611
url: /fr/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Spécifie le type d'ombre d'une forme.

 **Remarks:** 

ShadowType n'est pas un attribut simple, mais un préréglage qui définit en une fois plusieurs attributs qui composent l'apparence de l'ombre.

 **Examples:** 

Montre comment travailler avec le formatage d'ombre pour la forme.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Champs

| Champ | Description |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | Premier type d'ombre. |
| [SHADOW_10](#SHADOW-10) | Dixième type d'ombre. |
| [SHADOW_11](#SHADOW-11) | Onzième type d'ombre. |
| [SHADOW_12](#SHADOW-12) | Douzième type d'ombre. |
| [SHADOW_13](#SHADOW-13) | Treizième type d'ombre. |
| [SHADOW_14](#SHADOW-14) | Quatorzième type d'ombre. |
| [SHADOW_15](#SHADOW-15) | Quinzième type d'ombre. |
| [SHADOW_16](#SHADOW-16) | Seizième type d'ombre. |
| [SHADOW_17](#SHADOW-17) | Dix-septième type d'ombre. |
| [SHADOW_18](#SHADOW-18) | Dix-huitième type d'ombre. |
| [SHADOW_19](#SHADOW-19) | Dix-neuvième type d'ombre. |
| [SHADOW_2](#SHADOW-2) | Deuxième type d'ombre. |
| [SHADOW_20](#SHADOW-20) | Vingtième type d'ombre. |
| [SHADOW_21](#SHADOW-21) | Vingt-et-unième type d'ombre. |
| [SHADOW_22](#SHADOW-22) | Vingt-deuxième type d'ombre. |
| [SHADOW_23](#SHADOW-23) | Vingt-troisième type d'ombre. |
| [SHADOW_24](#SHADOW-24) | Vingt-quatrième type d'ombre. |
| [SHADOW_25](#SHADOW-25) | Vingt-cinquième type d'ombre. |
| [SHADOW_26](#SHADOW-26) | Vingt-sixième type d'ombre. |
| [SHADOW_27](#SHADOW-27) | Vingt-septième type d'ombre. |
| [SHADOW_28](#SHADOW-28) | Vingt-huitième type d'ombre. |
| [SHADOW_29](#SHADOW-29) | Vingt-neuvième type d'ombre. |
| [SHADOW_3](#SHADOW-3) | Troisième type d'ombre. |
| [SHADOW_30](#SHADOW-30) | Trentième type d'ombre. |
| [SHADOW_31](#SHADOW-31) | Trente-et-unième type d'ombre. |
| [SHADOW_32](#SHADOW-32) | Trente-deuxième type d'ombre. |
| [SHADOW_33](#SHADOW-33) | Trente-troisième type d'ombre. |
| [SHADOW_34](#SHADOW-34) | Trente-quatrième type d'ombre. |
| [SHADOW_35](#SHADOW-35) | Trente-cinquième type d'ombre. |
| [SHADOW_36](#SHADOW-36) | Trente-sixième type d'ombre. |
| [SHADOW_37](#SHADOW-37) | Trente-septième type d'ombre. |
| [SHADOW_38](#SHADOW-38) | Trente-huitième type d'ombre. |
| [SHADOW_39](#SHADOW-39) | Trente-neuvième type d'ombre. |
| [SHADOW_4](#SHADOW-4) | Quatrième type d'ombre. |
| [SHADOW_40](#SHADOW-40) | Quarantième type d'ombre. |
| [SHADOW_41](#SHADOW-41) | Quarante-et-unième type d'ombre. |
| [SHADOW_42](#SHADOW-42) | Quarante-deuxième type d'ombre. |
| [SHADOW_43](#SHADOW-43) | Quarante-troisième type d'ombre. |
| [SHADOW_5](#SHADOW-5) | Cinquième type d'ombre. |
| [SHADOW_6](#SHADOW-6) | Sixième type d'ombre. |
| [SHADOW_7](#SHADOW-7) | Septième type d'ombre. |
| [SHADOW_8](#SHADOW-8) | Huitième type d'ombre. |
| [SHADOW_9](#SHADOW-9) | Neuvième type d'ombre. |
| [SHADOW_MIXED](#SHADOW-MIXED) | Aucun des préréglages d'ombre prédéfinis. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


Premier type d'ombre.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Dixième type d'ombre.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


Onzième type d'ombre.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


Douzième type d'ombre.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


Treizième type d'ombre.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


Quatorzième type d'ombre.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


Quinzième type d'ombre.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


Seizième type d'ombre.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


Dix-septième type d'ombre.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


Dix-huitième type d'ombre.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


Dix-neuvième type d'ombre.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


Deuxième type d'ombre.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Vingtième type d'ombre.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Vingt-et-unième type d'ombre.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Vingt-deuxième type d'ombre.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Vingt-troisième type d'ombre.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Vingt-quatrième type d'ombre.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Vingt-cinquième type d'ombre.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Vingt-sixième type d'ombre.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Vingt-septième type d'ombre.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Vingt-huitième type d'ombre.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Vingt-neuvième type d'ombre.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Troisième type d'ombre.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Trentième type d'ombre.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Trente-et-unième type d'ombre.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Trente-deuxième type d'ombre.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Trente-troisième type d'ombre.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Trente-quatrième type d'ombre.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Trente-cinquième type d'ombre.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Trente-sixième type d'ombre.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Trente-septième type d'ombre.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Trente-huitième type d'ombre.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Trente-neuvième type d'ombre.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Quatrième type d'ombre.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Quarantième type d'ombre.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Quarante-et-unième type d'ombre.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Quarante-deuxième type d'ombre.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Quarante-troisième type d'ombre.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Cinquième type d'ombre.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Sixième type d'ombre.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Septième type d'ombre.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Huitième type d'ombre.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Neuvième type d'ombre.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


Aucun des préréglages d'ombre prédéfinis.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
