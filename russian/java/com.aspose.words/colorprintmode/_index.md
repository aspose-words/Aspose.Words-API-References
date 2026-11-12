---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как печатаются некрасочные страницы, если устройство поддерживает цветную печать в Java."
type: docs
weight: 106
url: /ru/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Указывает, как печатаются бесцветные страницы, если устройство поддерживает цветную печать.
## Поля

| Поле | Описание |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Обнаруженные некрасочные страницы печатаются в градациях серого. |
| [NORMAL](#NORMAL) | Все страницы печатаются в соответствии с возможностями и настройками принтера. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Обнаруженные некрасочные страницы печатаются в градациях серого.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) автоматически устанавливается в false для обнаруженных некрасочных страниц. Если принтер не поддерживает цветную печать, этот параметр игнорируется.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Все страницы печатаются в соответствии с возможностями и настройками принтера.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorPrintMode) {#toString-int}
```
public static String toString(int colorPrintMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
