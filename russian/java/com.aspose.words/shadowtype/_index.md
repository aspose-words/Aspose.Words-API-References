---
title: "ShadowType"
linktitle: "ShadowType"
second_title: "Aspose.Words для Java"
description: "Указывает тип тени формы в Java."
type: docs
weight: 611
url: /ru/java/com.aspose.words/shadowtype/
---

**Inheritance:**
java.lang.Object
```
public class ShadowType
```

Указывает тип тени фигуры.

 **Remarks:** 

ShadowType не является простым атрибутом, а предустановкой, которая сразу задаёт несколько атрибутов, формирующих внешний вид тени.

 **Examples:** 

Показывает, как работать с форматированием тени для формы.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [SHADOW_1](#SHADOW-1) | Первый тип тени. |
| [SHADOW_10](#SHADOW-10) | Десятый тип тени. |
| [SHADOW_11](#SHADOW-11) | Одиннадцатый тип тени. |
| [SHADOW_12](#SHADOW-12) | Двенадцатый тип тени. |
| [SHADOW_13](#SHADOW-13) | Тринадцатый тип тени. |
| [SHADOW_14](#SHADOW-14) | Четырнадцатый тип тени. |
| [SHADOW_15](#SHADOW-15) | Пятнадцатый тип тени. |
| [SHADOW_16](#SHADOW-16) | Шестнадцатый тип тени. |
| [SHADOW_17](#SHADOW-17) | Семнадцатый тип тени. |
| [SHADOW_18](#SHADOW-18) | Восемнадцатый тип тени. |
| [SHADOW_19](#SHADOW-19) | Девятнадцатый тип тени. |
| [SHADOW_2](#SHADOW-2) | Второй тип тени. |
| [SHADOW_20](#SHADOW-20) | Двадцатый тип тени. |
| [SHADOW_21](#SHADOW-21) | Двадцать первый тип тени. |
| [SHADOW_22](#SHADOW-22) | Двадцать второй тип тени. |
| [SHADOW_23](#SHADOW-23) | Двадцать третий тип тени. |
| [SHADOW_24](#SHADOW-24) | Двадцать четвертый тип тени. |
| [SHADOW_25](#SHADOW-25) | Двадцать пятый тип тени. |
| [SHADOW_26](#SHADOW-26) | Двадцать шестой тип тени. |
| [SHADOW_27](#SHADOW-27) | Двадцать седьмой тип тени. |
| [SHADOW_28](#SHADOW-28) | Двадцать восьмой тип тени. |
| [SHADOW_29](#SHADOW-29) | Двадцать девятый тип тени. |
| [SHADOW_3](#SHADOW-3) | Третий тип тени. |
| [SHADOW_30](#SHADOW-30) | Тридцатый тип тени. |
| [SHADOW_31](#SHADOW-31) | Тридцать первый тип тени. |
| [SHADOW_32](#SHADOW-32) | Тридцать второй тип тени. |
| [SHADOW_33](#SHADOW-33) | Тридцать третий тип тени. |
| [SHADOW_34](#SHADOW-34) | Тридцать четвертый тип тени. |
| [SHADOW_35](#SHADOW-35) | Тридцать пятый тип тени. |
| [SHADOW_36](#SHADOW-36) | Тридцать шестой тип тени. |
| [SHADOW_37](#SHADOW-37) | Тридцать седьмой тип тени. |
| [SHADOW_38](#SHADOW-38) | Тридцать восьмой тип тени. |
| [SHADOW_39](#SHADOW-39) | Тридцать девятый тип тени. |
| [SHADOW_4](#SHADOW-4) | Четвертый тип тени. |
| [SHADOW_40](#SHADOW-40) | Сороковой тип тени. |
| [SHADOW_41](#SHADOW-41) | Сорок первый тип тени. |
| [SHADOW_42](#SHADOW-42) | Сорок второй тип тени. |
| [SHADOW_43](#SHADOW-43) | Сорок третий тип тени. |
| [SHADOW_5](#SHADOW-5) | Пятый тип тени. |
| [SHADOW_6](#SHADOW-6) | Шестой тип тени. |
| [SHADOW_7](#SHADOW-7) | Седьмой тип тени. |
| [SHADOW_8](#SHADOW-8) | Восьмой тип тени. |
| [SHADOW_9](#SHADOW-9) | Девятый тип тени. |
| [SHADOW_MIXED](#SHADOW-MIXED) | Нет предустановленных пресетов теней. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String shadowTypeName)](#fromName-java.lang.String) |  |
| [getName(int shadowType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shadowType)](#toString-int) |  |
### SHADOW_1 {#SHADOW-1}
```
public static int SHADOW_1
```


Первый тип тени.

### SHADOW_10 {#SHADOW-10}
```
public static int SHADOW_10
```


Десятый тип тени.

### SHADOW_11 {#SHADOW-11}
```
public static int SHADOW_11
```


Одиннадцатый тип тени.

### SHADOW_12 {#SHADOW-12}
```
public static int SHADOW_12
```


Двенадцатый тип тени.

### SHADOW_13 {#SHADOW-13}
```
public static int SHADOW_13
```


Тринадцатый тип тени.

### SHADOW_14 {#SHADOW-14}
```
public static int SHADOW_14
```


Четырнадцатый тип тени.

### SHADOW_15 {#SHADOW-15}
```
public static int SHADOW_15
```


Пятнадцатый тип тени.

### SHADOW_16 {#SHADOW-16}
```
public static int SHADOW_16
```


Шестнадцатый тип тени.

### SHADOW_17 {#SHADOW-17}
```
public static int SHADOW_17
```


Семнадцатый тип тени.

### SHADOW_18 {#SHADOW-18}
```
public static int SHADOW_18
```


Восемнадцатый тип тени.

### SHADOW_19 {#SHADOW-19}
```
public static int SHADOW_19
```


Девятнадцатый тип тени.

### SHADOW_2 {#SHADOW-2}
```
public static int SHADOW_2
```


Второй тип тени.

### SHADOW_20 {#SHADOW-20}
```
public static int SHADOW_20
```


Двадцатый тип тени.

### SHADOW_21 {#SHADOW-21}
```
public static int SHADOW_21
```


Двадцать первый тип тени.

### SHADOW_22 {#SHADOW-22}
```
public static int SHADOW_22
```


Двадцать второй тип тени.

### SHADOW_23 {#SHADOW-23}
```
public static int SHADOW_23
```


Двадцать третий тип тени.

### SHADOW_24 {#SHADOW-24}
```
public static int SHADOW_24
```


Двадцать четвертый тип тени.

### SHADOW_25 {#SHADOW-25}
```
public static int SHADOW_25
```


Двадцать пятый тип тени.

### SHADOW_26 {#SHADOW-26}
```
public static int SHADOW_26
```


Двадцать шестой тип тени.

### SHADOW_27 {#SHADOW-27}
```
public static int SHADOW_27
```


Двадцать седьмой тип тени.

### SHADOW_28 {#SHADOW-28}
```
public static int SHADOW_28
```


Двадцать восьмой тип тени.

### SHADOW_29 {#SHADOW-29}
```
public static int SHADOW_29
```


Двадцать девятый тип тени.

### SHADOW_3 {#SHADOW-3}
```
public static int SHADOW_3
```


Третий тип тени.

### SHADOW_30 {#SHADOW-30}
```
public static int SHADOW_30
```


Тридцатый тип тени.

### SHADOW_31 {#SHADOW-31}
```
public static int SHADOW_31
```


Тридцать первый тип тени.

### SHADOW_32 {#SHADOW-32}
```
public static int SHADOW_32
```


Тридцать второй тип тени.

### SHADOW_33 {#SHADOW-33}
```
public static int SHADOW_33
```


Тридцать третий тип тени.

### SHADOW_34 {#SHADOW-34}
```
public static int SHADOW_34
```


Тридцать четвертый тип тени.

### SHADOW_35 {#SHADOW-35}
```
public static int SHADOW_35
```


Тридцать пятый тип тени.

### SHADOW_36 {#SHADOW-36}
```
public static int SHADOW_36
```


Тридцать шестой тип тени.

### SHADOW_37 {#SHADOW-37}
```
public static int SHADOW_37
```


Тридцать седьмой тип тени.

### SHADOW_38 {#SHADOW-38}
```
public static int SHADOW_38
```


Тридцать восьмой тип тени.

### SHADOW_39 {#SHADOW-39}
```
public static int SHADOW_39
```


Тридцать девятый тип тени.

### SHADOW_4 {#SHADOW-4}
```
public static int SHADOW_4
```


Четвертый тип тени.

### SHADOW_40 {#SHADOW-40}
```
public static int SHADOW_40
```


Сороковой тип тени.

### SHADOW_41 {#SHADOW-41}
```
public static int SHADOW_41
```


Сорок первый тип тени.

### SHADOW_42 {#SHADOW-42}
```
public static int SHADOW_42
```


Сорок второй тип тени.

### SHADOW_43 {#SHADOW-43}
```
public static int SHADOW_43
```


Сорок третий тип тени.

### SHADOW_5 {#SHADOW-5}
```
public static int SHADOW_5
```


Пятый тип тени.

### SHADOW_6 {#SHADOW-6}
```
public static int SHADOW_6
```


Шестой тип тени.

### SHADOW_7 {#SHADOW-7}
```
public static int SHADOW_7
```


Седьмой тип тени.

### SHADOW_8 {#SHADOW-8}
```
public static int SHADOW_8
```


Восьмой тип тени.

### SHADOW_9 {#SHADOW-9}
```
public static int SHADOW_9
```


Девятый тип тени.

### SHADOW_MIXED {#SHADOW-MIXED}
```
public static int SHADOW_MIXED
```


Нет предустановленных пресетов теней.

### length {#length}
```
public static int length
```


### fromName(String shadowTypeName) {#fromName-java.lang.String}
```
public static int fromName(String shadowTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shadowTypeName | java.lang.String |  |

**Returns:**
int
### getName(int shadowType) {#getName-int}
```
public static String getName(int shadowType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| shadowType | int |  |

**Returns:**
java.lang.String
