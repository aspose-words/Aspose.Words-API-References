---
title: MathObjectType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип объекта Office Math.
type: docs
weight: 391
url: /ru/java/com.aspose.words/mathobjecttype/
---

**Наследование:**
java.lang.Object
```
public class MathObjectType
```

Указывает тип объекта Office Math.
## Поля

| Поле | Описание |
| --- | --- |
| [ACCENT](#ACCENT) | Акцентная функция, состоящая из основы и объединяющего диакритического знака. |
| [ARGUMENT](#ARGUMENT) | Объект аргумента. |
| [ARRAY](#ARRAY) | Объект-массив, состоящий из одного или нескольких уравнений, выражений или другого математического текста, который может быть выровнен по вертикали как единое целое по отношению к окружающему тексту в строке. |
| [BAR](#BAR) | Функция полосы, состоящая из базового аргумента и верхней или нижней черты. |
| [BORDER_BOX](#BORDER-BOX) | Объект Border Box, состоящий из границы, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения). |
| [BOX](#BOX) | Объект Box, который используется для группировки компонентов уравнения или другого экземпляра математического текста. |
| [DEGREE](#DEGREE) | Степень в математическом радикале. |
| [DELIMITER](#DELIMITER) | Объект-разделитель, состоящий из открывающих и закрывающих разделителей (таких как круглые и фигурные скобки, квадратные скобки и вертикальные полосы) и элемента, содержащегося внутри. |
| [DENOMINATOR](#DENOMINATOR) | Знаменатель дробного объекта. |
| [FRACTION](#FRACTION) | Дробный объект, состоящий из числителя и знаменателя, разделенных чертой дроби. |
| [FUNCTION](#FUNCTION) | Объект Function-Apply, который состоит из имени функции и элемента аргумента, на который воздействует. |
| [FUNCTION_NAME](#FUNCTION-NAME) | Имя функции. |
| [GROUP_CHARACTER](#GROUP-CHARACTER) | Объект Group-Character, состоящий из символа, нарисованного над или под текстом, часто с целью визуального группирования элементов. |
| [LIMIT](#LIMIT) |  Нижний предел[LOWER\_LIMIT](../../com.aspose.words/mathobjecttype\#LOWER-LIMIT) объекта и верхний предел[UPPER\_LIMIT](../../com.aspose.words/mathobjecttype\#UPPER-LIMIT) функция. |
| [LOWER_LIMIT](#LOWER-LIMIT) | Объект нижнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно под ним. |
| [MATRIX](#MATRIX) | Матричный объект, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одном или нескольких столбцах. |
| [MATRIX_ROW](#MATRIX-ROW) | Одна строка матрицы. |
| [NUMERATOR](#NUMERATOR) | Числитель объекта Fraction. |
| [N_ARY](#N-ARY) | N-мерный объект, состоящий из n-мерного объекта, основания (или операнда) и необязательных верхнего и нижнего пределов. |
| [O_MATH](#O-MATH) | Экземпляр математического текста. |
| [O_MATH_PARA](#O-MATH-PARA) |  Математический абзац или отображаемая математическая зона, содержащая один или несколько[O\_MATH](../../com.aspose.words/mathobjecttype\#O-MATH) элементы, находящиеся в режиме отображения. |
| [PHANTOM](#PHANTOM) | Фантомный объект. |
| [PRE_SUB_SUPERSCRIPT](#PRE-SUB-SUPERSCRIPT) | Объект Pre-Sub-Superscript, который состоит из базового элемента и нижнего и верхнего индексов, расположенных слева от базового. |
| [RADICAL](#RADICAL) | Радикальный объект, состоящий из радикала, базового элемента и необязательной степени. |
| [SUBSCRIPT](#SUBSCRIPT) | Объект нижнего индекса, который состоит из базового элемента и скрипта уменьшенного размера, расположенного ниже и правее. |
| [SUBSCRIPT_PART](#SUBSCRIPT-PART) | Подстрочный индекс объекта, который может иметь подстрочную часть. |
| [SUB_SUPERSCRIPT](#SUB-SUPERSCRIPT) | Поднадстрочный объект, состоящий из базового элемента, шрифта уменьшенного размера, расположенного ниже и правее, и скрипта уменьшенного размера, расположенного выше и правее. |
| [SUPERCRIPT](#SUPERCRIPT) | Надстрочный объект, состоящий из базового элемента и шрифта уменьшенного размера, расположенного сверху и справа. |
| [SUPERSCRIPT_PART](#SUPERSCRIPT-PART) | Верхний индекс надстрочного объекта. |
| [UPPER_LIMIT](#UPPER-LIMIT) | Объект Upper-Limit, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно над ним. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String mathObjectTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int mathObjectType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int mathObjectType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ACCENT {#ACCENT}
```
public static int ACCENT
```


Акцентная функция, состоящая из основы и объединяющего диакритического знака.

### ARGUMENT {#ARGUMENT}
```
public static int ARGUMENT
```


Объект аргумента. Закрывает объекты Office Math, когда они используются в качестве аргументов для других объектов Office Math.

### ARRAY {#ARRAY}
```
public static int ARRAY
```


Объект-массив, состоящий из одного или нескольких уравнений, выражений или другого математического текста, который может быть выровнен по вертикали как единое целое по отношению к окружающему тексту в строке.

### BAR {#BAR}
```
public static int BAR
```


Функция полосы, состоящая из базового аргумента и верхней или нижней черты.

### BORDER_BOX {#BORDER-BOX}
```
public static int BORDER_BOX
```


Объект Border Box, состоящий из границы, нарисованной вокруг экземпляра математического текста (например, формулы или уравнения).

### BOX {#BOX}
```
public static int BOX
```


Объект Box, который используется для группировки компонентов уравнения или другого экземпляра математического текста.

### DEGREE {#DEGREE}
```
public static int DEGREE
```


Степень в математическом радикале.

### DELIMITER {#DELIMITER}
```
public static int DELIMITER
```


Объект-разделитель, состоящий из открывающих и закрывающих разделителей (таких как круглые и фигурные скобки, квадратные скобки и вертикальные полосы) и элемента, содержащегося внутри.

### DENOMINATOR {#DENOMINATOR}
```
public static int DENOMINATOR
```


Знаменатель дробного объекта.

### FRACTION {#FRACTION}
```
public static int FRACTION
```


Дробный объект, состоящий из числителя и знаменателя, разделенных чертой дроби.

### FUNCTION {#FUNCTION}
```
public static int FUNCTION
```


Объект Function-Apply, который состоит из имени функции и элемента аргумента, на который воздействует.

### FUNCTION_NAME {#FUNCTION-NAME}
```
public static int FUNCTION_NAME
```


Имя функции. Например, имена функций — sin и cos.

### GROUP_CHARACTER {#GROUP-CHARACTER}
```
public static int GROUP_CHARACTER
```


Объект Group-Character, состоящий из символа, нарисованного над или под текстом, часто с целью визуального группирования элементов.

### LIMIT {#LIMIT}
```
public static int LIMIT
```


 Нижний предел[LOWER\_LIMIT](../../com.aspose.words/mathobjecttype\#LOWER-LIMIT) объекта и верхний предел[UPPER\_LIMIT](../../com.aspose.words/mathobjecttype\#UPPER-LIMIT) функция.

### LOWER_LIMIT {#LOWER-LIMIT}
```
public static int LOWER_LIMIT
```


Объект нижнего предела, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно под ним.

### MATRIX {#MATRIX}
```
public static int MATRIX
```


Матричный объект, состоящий из одного или нескольких элементов, расположенных в одной или нескольких строках и одном или нескольких столбцах.

### MATRIX_ROW {#MATRIX-ROW}
```
public static int MATRIX_ROW
```


Одна строка матрицы.

### NUMERATOR {#NUMERATOR}
```
public static int NUMERATOR
```


Числитель объекта Fraction.

### N_ARY {#N-ARY}
```
public static int N_ARY
```


N-мерный объект, состоящий из n-мерного объекта, основания (или операнда) и необязательных верхнего и нижнего пределов.

### O_MATH {#O-MATH}
```
public static int O_MATH
```


Экземпляр математического текста.

### O_MATH_PARA {#O-MATH-PARA}
```
public static int O_MATH_PARA
```


 Математический абзац или отображаемая математическая зона, содержащая один или несколько[O\_MATH](../../com.aspose.words/mathobjecttype\#O-MATH) элементы, находящиеся в режиме отображения.

### PHANTOM {#PHANTOM}
```
public static int PHANTOM
```


Фантомный объект.

### PRE_SUB_SUPERSCRIPT {#PRE-SUB-SUPERSCRIPT}
```
public static int PRE_SUB_SUPERSCRIPT
```


Объект Pre-Sub-Superscript, который состоит из базового элемента и нижнего и верхнего индексов, расположенных слева от базового.

### RADICAL {#RADICAL}
```
public static int RADICAL
```


Радикальный объект, состоящий из радикала, базового элемента и необязательной степени.

### SUBSCRIPT {#SUBSCRIPT}
```
public static int SUBSCRIPT
```


Объект нижнего индекса, который состоит из базового элемента и скрипта уменьшенного размера, расположенного ниже и правее.

### SUBSCRIPT_PART {#SUBSCRIPT-PART}
```
public static int SUBSCRIPT_PART
```


Подстрочный индекс объекта, который может иметь подстрочную часть.

### SUB_SUPERSCRIPT {#SUB-SUPERSCRIPT}
```
public static int SUB_SUPERSCRIPT
```


Поднадстрочный объект, состоящий из базового элемента, шрифта уменьшенного размера, расположенного ниже и правее, и скрипта уменьшенного размера, расположенного выше и правее.

### SUPERCRIPT {#SUPERCRIPT}
```
public static int SUPERCRIPT
```


Надстрочный объект, состоящий из базового элемента и шрифта уменьшенного размера, расположенного сверху и справа.

### SUPERSCRIPT_PART {#SUPERSCRIPT-PART}
```
public static int SUPERSCRIPT_PART
```


Верхний индекс надстрочного объекта.

### UPPER_LIMIT {#UPPER-LIMIT}
```
public static int UPPER_LIMIT
```


Объект Upper-Limit, состоящий из текста на базовой линии и текста уменьшенного размера непосредственно над ним.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String mathObjectTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String mathObjectTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mathObjectTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int mathObjectType) {#getName-int-}
```
public static String getName(int mathObjectType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mathObjectType | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int mathObjectType) {#toString-int-}
```
public static String toString(int mathObjectType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mathObjectType | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
