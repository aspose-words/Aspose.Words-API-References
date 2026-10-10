---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع ظل الشكل في جافا."
type: docs
weight: 611
url: /ar/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

يحدد نوع ظل الشكل.

 **Remarks:** 

ShadowType ليس سمة بسيطة، بل إعداد مسبق يحدد في آن واحد عدة سمات تشكل مظهر الظل.

 **Examples:** 

يظهر كيفية العمل مع تنسيق الظل للشكل.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | النوع الأول للظل. |
| [SHADOW_10](#SHADOW-10) | النوع العاشر للظل. |
| [SHADOW_11](#SHADOW-11) | النوع الحادي عشر من الظل. |
| [SHADOW_12](#SHADOW-12) | النوع الثاني عشر من الظل. |
| [SHADOW_13](#SHADOW-13) | النوع الثالث عشر من الظل. |
| [SHADOW_14](#SHADOW-14) | النوع الرابع عشر من الظل. |
| [SHADOW_15](#SHADOW-15) | النوع الخامس عشر من الظل. |
| [SHADOW_16](#SHADOW-16) | النوع السادس عشر من الظل. |
| [SHADOW_17](#SHADOW-17) | النوع السابع عشر من الظل. |
| [SHADOW_18](#SHADOW-18) | النوع الثامن عشر من الظل. |
| [SHADOW_19](#SHADOW-19) | النوع التاسع عشر من الظل. |
| [SHADOW_2](#SHADOW-2) | النوع الثاني من الظل. |
| [SHADOW_20](#SHADOW-20) | النوع العشرون من الظل. |
| [SHADOW_21](#SHADOW-21) | النوع الحادي والعشرون من الظل. |
| [SHADOW_22](#SHADOW-22) | النوع الثاني والعشرون من الظل. |
| [SHADOW_23](#SHADOW-23) | النوع الثالث والعشرون من الظل. |
| [SHADOW_24](#SHADOW-24) | النوع الرابع والعشرون من الظل. |
| [SHADOW_25](#SHADOW-25) | النوع الخامس والعشرون من الظل. |
| [SHADOW_26](#SHADOW-26) | النوع السادس والعشرون من الظل. |
| [SHADOW_27](#SHADOW-27) | النوع السابع والعشرون من الظل. |
| [SHADOW_28](#SHADOW-28) | النوع الثامن والعشرون من الظل. |
| [SHADOW_29](#SHADOW-29) | النوع التاسع والعشرون من الظل. |
| [SHADOW_3](#SHADOW-3) | النوع الثالث من الظل. |
| [SHADOW_30](#SHADOW-30) | النوع الثلاثون من الظل. |
| [SHADOW_31](#SHADOW-31) | النوع الحادي والثلاثون من الظل. |
| [SHADOW_32](#SHADOW-32) | النوع الثاني والثلاثون من الظل. |
| [SHADOW_33](#SHADOW-33) | النوع الثالث والثلاثون من الظل. |
| [SHADOW_34](#SHADOW-34) | نوع الظل الرابع والثلاثين. |
| [SHADOW_35](#SHADOW-35) | نوع الظل الخامس والثلاثين. |
| [SHADOW_36](#SHADOW-36) | نوع الظل السادس والثلاثين. |
| [SHADOW_37](#SHADOW-37) | نوع الظل السابع والثلاثين. |
| [SHADOW_38](#SHADOW-38) | نوع الظل الثامن والثلاثين. |
| [SHADOW_39](#SHADOW-39) | نوع الظل التاسع والثلاثين. |
| [SHADOW_4](#SHADOW-4) | نوع الظل الرابع. |
| [SHADOW_40](#SHADOW-40) | نوع الظل الأربعين. |
| [SHADOW_41](#SHADOW-41) | نوع الظل الحادي والأربعين. |
| [SHADOW_42](#SHADOW-42) | نوع الظل الثاني والأربعين. |
| [SHADOW_43](#SHADOW-43) | نوع الظل الثالث والأربعين. |
| [SHADOW_5](#SHADOW-5) | نوع الظل الخامس. |
| [SHADOW_6](#SHADOW-6) | نوع الظل السادس. |
| [SHADOW_7](#SHADOW-7) | نوع الظل السابع. |
| [SHADOW_8](#SHADOW-8) | نوع الظل الثامن. |
| [SHADOW_9](#SHADOW-9) | نوع الظل التاسع. |
| [SHADOW_MIXED](#SHADOW-MIXED) | لا توجد إعدادات ظل مسبقة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


النوع الأول للظل.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


النوع العاشر للظل.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


النوع الحادي عشر من الظل.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


النوع الثاني عشر من الظل.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


النوع الثالث عشر من الظل.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


النوع الرابع عشر من الظل.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


النوع الخامس عشر من الظل.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


النوع السادس عشر من الظل.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


النوع السابع عشر من الظل.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


النوع الثامن عشر من الظل.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


النوع التاسع عشر من الظل.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


النوع الثاني من الظل.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


النوع العشرون من الظل.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


النوع الحادي والعشرون من الظل.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


النوع الثاني والعشرون من الظل.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


النوع الثالث والعشرون من الظل.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


النوع الرابع والعشرون من الظل.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


النوع الخامس والعشرون من الظل.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


النوع السادس والعشرون من الظل.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


النوع السابع والعشرون من الظل.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


النوع الثامن والعشرون من الظل.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


النوع التاسع والعشرون من الظل.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


النوع الثالث من الظل.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


النوع الثلاثون من الظل.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


النوع الحادي والثلاثون من الظل.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


النوع الثاني والثلاثون من الظل.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


النوع الثالث والثلاثون من الظل.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


نوع الظل الرابع والثلاثين.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


نوع الظل الخامس والثلاثين.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


نوع الظل السادس والثلاثين.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


نوع الظل السابع والثلاثين.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


نوع الظل الثامن والثلاثين.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


نوع الظل التاسع والثلاثين.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


نوع الظل الرابع.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


نوع الظل الأربعين.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


نوع الظل الحادي والأربعين.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


نوع الظل الثاني والأربعين.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


نوع الظل الثالث والأربعين.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


نوع الظل الخامس.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


نوع الظل السادس.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


نوع الظل السابع.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


نوع الظل الثامن.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


نوع الظل التاسع.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


لا توجد إعدادات ظل مسبقة.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
