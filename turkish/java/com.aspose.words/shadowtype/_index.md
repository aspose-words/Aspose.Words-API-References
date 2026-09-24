---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekil gölgesinin tipini belirtir."
type: docs
weight: 611
url: /tr/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Bir şekil gölgesinin türünü belirtir.

 **Remarks:** 

ShadowType basit bir öznitelik değildir; gölge görünümünü oluşturan birkaç özniteliği bir anda ayarlayan bir ön ayardır.

 **Examples:** 

Şekil için gölge biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | İlk gölge tipi. |
| [SHADOW_10](#SHADOW-10) | Onuncu gölge tipi. |
| [SHADOW_11](#SHADOW-11) | On birinci gölge türü. |
| [SHADOW_12](#SHADOW-12) | On ikinci gölge türü. |
| [SHADOW_13](#SHADOW-13) | On üçüncü gölge türü. |
| [SHADOW_14](#SHADOW-14) | On dördüncü gölge türü. |
| [SHADOW_15](#SHADOW-15) | On beşinci gölge türü. |
| [SHADOW_16](#SHADOW-16) | On altıncı gölge türü. |
| [SHADOW_17](#SHADOW-17) | On yedinci gölge türü. |
| [SHADOW_18](#SHADOW-18) | On sekizinci gölge türü. |
| [SHADOW_19](#SHADOW-19) | On dokuzuncu gölge türü. |
| [SHADOW_2](#SHADOW-2) | İkinci gölge türü. |
| [SHADOW_20](#SHADOW-20) | Yirminci gölge türü. |
| [SHADOW_21](#SHADOW-21) | Yirmi birinci gölge türü. |
| [SHADOW_22](#SHADOW-22) | Yirmi ikinci gölge türü. |
| [SHADOW_23](#SHADOW-23) | Yirmi üçüncü gölge türü. |
| [SHADOW_24](#SHADOW-24) | Yirmi dördüncü gölge türü. |
| [SHADOW_25](#SHADOW-25) | Yirmi beşinci gölge türü. |
| [SHADOW_26](#SHADOW-26) | Yirmi altıncı gölge türü. |
| [SHADOW_27](#SHADOW-27) | Yirmi yedinci gölge türü. |
| [SHADOW_28](#SHADOW-28) | Yirmi sekizinci gölge türü. |
| [SHADOW_29](#SHADOW-29) | Yirmi dokuzuncu gölge türü. |
| [SHADOW_3](#SHADOW-3) | Üçüncü gölge türü. |
| [SHADOW_30](#SHADOW-30) | Otuzuncu gölge türü. |
| [SHADOW_31](#SHADOW-31) | Otuz birinci gölge türü. |
| [SHADOW_32](#SHADOW-32) | Otuz ikinci gölge türü. |
| [SHADOW_33](#SHADOW-33) | Otuz üçüncü gölge türü. |
| [SHADOW_34](#SHADOW-34) | Otuz dördüncü gölge tipi. |
| [SHADOW_35](#SHADOW-35) | Otuz beşinci gölge tipi. |
| [SHADOW_36](#SHADOW-36) | Otuz altıncı gölge tipi. |
| [SHADOW_37](#SHADOW-37) | Otuz yedinci gölge tipi. |
| [SHADOW_38](#SHADOW-38) | Otuz sekizinci gölge tipi. |
| [SHADOW_39](#SHADOW-39) | Otuz dokuzuncu gölge tipi. |
| [SHADOW_4](#SHADOW-4) | Dördüncü gölge tipi. |
| [SHADOW_40](#SHADOW-40) | Kırkıncı gölge tipi. |
| [SHADOW_41](#SHADOW-41) | Kırk birinci gölge tipi. |
| [SHADOW_42](#SHADOW-42) | Kırk ikinci gölge tipi. |
| [SHADOW_43](#SHADOW-43) | Kırk üçüncü gölge tipi. |
| [SHADOW_5](#SHADOW-5) | Beşinci gölge tipi. |
| [SHADOW_6](#SHADOW-6) | Altıncı gölge tipi. |
| [SHADOW_7](#SHADOW-7) | Yedinci gölge tipi. |
| [SHADOW_8](#SHADOW-8) | Sekizinci gölge tipi. |
| [SHADOW_9](#SHADOW-9) | Dokuzuncu gölge tipi. |
| [SHADOW_MIXED](#SHADOW-MIXED) | Önceden tanımlanmış gölge ön ayarlarından hiçbiri. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


İlk gölge tipi.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Onuncu gölge tipi.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


On birinci gölge türü.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


On ikinci gölge türü.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


On üçüncü gölge türü.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


On dördüncü gölge türü.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


On beşinci gölge türü.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


On altıncı gölge türü.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


On yedinci gölge türü.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


On sekizinci gölge türü.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


On dokuzuncu gölge türü.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


İkinci gölge türü.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Yirminci gölge türü.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Yirmi birinci gölge türü.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Yirmi ikinci gölge türü.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Yirmi üçüncü gölge türü.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Yirmi dördüncü gölge türü.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Yirmi beşinci gölge türü.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Yirmi altıncı gölge türü.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Yirmi yedinci gölge türü.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Yirmi sekizinci gölge türü.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Yirmi dokuzuncu gölge türü.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Üçüncü gölge türü.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Otuzuncu gölge türü.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Otuz birinci gölge türü.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Otuz ikinci gölge türü.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Otuz üçüncü gölge türü.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Otuz dördüncü gölge tipi.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Otuz beşinci gölge tipi.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Otuz altıncı gölge tipi.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Otuz yedinci gölge tipi.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Otuz sekizinci gölge tipi.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Otuz dokuzuncu gölge tipi.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Dördüncü gölge tipi.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Kırkıncı gölge tipi.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Kırk birinci gölge tipi.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Kırk ikinci gölge tipi.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Kırk üçüncü gölge tipi.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Beşinci gölge tipi.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Altıncı gölge tipi.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Yedinci gölge tipi.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Sekizinci gölge tipi.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Dokuzuncu gölge tipi.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


Önceden tanımlanmış gölge ön ayarlarından hiçbiri.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
