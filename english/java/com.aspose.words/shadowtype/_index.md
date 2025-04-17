---
title: ShadowType
linktitle: ShadowType
second_title: Aspose.Words for Java
description: Specifies the type of a shape shadow in Java.
type: docs
weight: 600
url: /java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Specifies the type of a shape shadow.

 **Remarks:** 

ShadowType is not a simple attribute, but a preset that sets at once several attributes which form the shadow appearance.

 **Examples:** 

Shows how to work with a shadow formatting for the shape.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Fields

| Field | Description |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | First shadow type. |
| [SHADOW_10](#SHADOW-10) | Tenth shadow type. |
| [SHADOW_11](#SHADOW-11) | Eleventh shadow type. |
| [SHADOW_12](#SHADOW-12) | Twelfth shadow type. |
| [SHADOW_13](#SHADOW-13) | Thirteenth shadow type. |
| [SHADOW_14](#SHADOW-14) | Fourteenth shadow type. |
| [SHADOW_15](#SHADOW-15) | Fifteenth shadow type. |
| [SHADOW_16](#SHADOW-16) | Sixteenth shadow type. |
| [SHADOW_17](#SHADOW-17) | Seventeenth shadow type. |
| [SHADOW_18](#SHADOW-18) | Eighteenth shadow type. |
| [SHADOW_19](#SHADOW-19) | Nineteenth shadow type. |
| [SHADOW_2](#SHADOW-2) | Second shadow type. |
| [SHADOW_20](#SHADOW-20) | Twentieth shadow type. |
| [SHADOW_21](#SHADOW-21) | Twenty first shadow type. |
| [SHADOW_22](#SHADOW-22) | Twenty second shadow type. |
| [SHADOW_23](#SHADOW-23) | Twenty third shadow type. |
| [SHADOW_24](#SHADOW-24) | Twenty forth shadow type. |
| [SHADOW_25](#SHADOW-25) | Twenty fifth shadow type. |
| [SHADOW_26](#SHADOW-26) | Twenty sixth shadow type. |
| [SHADOW_27](#SHADOW-27) | Twenty seventh shadow type. |
| [SHADOW_28](#SHADOW-28) | Twenty eighth shadow type. |
| [SHADOW_29](#SHADOW-29) | Twenty ninth shadow type. |
| [SHADOW_3](#SHADOW-3) | Third shadow type. |
| [SHADOW_30](#SHADOW-30) | Thirtieth shadow type. |
| [SHADOW_31](#SHADOW-31) | Thirty first shadow type. |
| [SHADOW_32](#SHADOW-32) | Thirty second shadow type. |
| [SHADOW_33](#SHADOW-33) | Thirty third shadow type. |
| [SHADOW_34](#SHADOW-34) | Thirty forth shadow type. |
| [SHADOW_35](#SHADOW-35) | Thirty fifth shadow type. |
| [SHADOW_36](#SHADOW-36) | Thirty sixth shadow type. |
| [SHADOW_37](#SHADOW-37) | Thirty seventh shadow type. |
| [SHADOW_38](#SHADOW-38) | Thirty eighth shadow type. |
| [SHADOW_39](#SHADOW-39) | Thirty ninth shadow type. |
| [SHADOW_4](#SHADOW-4) | Fourth shadow type. |
| [SHADOW_40](#SHADOW-40) | Fortieth shadow type. |
| [SHADOW_41](#SHADOW-41) | Forty first shadow type. |
| [SHADOW_42](#SHADOW-42) | Forty second shadow type. |
| [SHADOW_43](#SHADOW-43) | Forty third shadow type. |
| [SHADOW_5](#SHADOW-5) | Fifth shadow type. |
| [SHADOW_6](#SHADOW-6) | Sixth shadow type. |
| [SHADOW_7](#SHADOW-7) | Seventh shadow type. |
| [SHADOW_8](#SHADOW-8) | Eighth shadow type. |
| [SHADOW_9](#SHADOW-9) | Ninth shadow type. |
| [SHADOW_MIXED](#SHADOW-MIXED) | None of predefined shadow presets. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


First shadow type.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Tenth shadow type.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


Eleventh shadow type.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


Twelfth shadow type.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


Thirteenth shadow type.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


Fourteenth shadow type.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


Fifteenth shadow type.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


Sixteenth shadow type.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


Seventeenth shadow type.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


Eighteenth shadow type.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


Nineteenth shadow type.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


Second shadow type.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Twentieth shadow type.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Twenty first shadow type.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Twenty second shadow type.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Twenty third shadow type.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Twenty forth shadow type.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Twenty fifth shadow type.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Twenty sixth shadow type.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Twenty seventh shadow type.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Twenty eighth shadow type.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Twenty ninth shadow type.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Third shadow type.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Thirtieth shadow type.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Thirty first shadow type.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Thirty second shadow type.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Thirty third shadow type.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Thirty forth shadow type.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Thirty fifth shadow type.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Thirty sixth shadow type.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Thirty seventh shadow type.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Thirty eighth shadow type.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Thirty ninth shadow type.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Fourth shadow type.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Fortieth shadow type.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Forty first shadow type.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Forty second shadow type.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Forty third shadow type.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Fifth shadow type.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Sixth shadow type.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Seventh shadow type.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Eighth shadow type.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Ninth shadow type.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


None of predefined shadow presets.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
