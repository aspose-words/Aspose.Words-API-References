---
title: ZoomType
second_title: Справочник по API Aspose.Words для Java
description: Возможные значения размера документа, отображаемого на экране в Microsoft Word.
type: docs
weight: 631
url: /ru/java/com.aspose.words/zoomtype/
---

**Наследование:**
java.lang.Object
```
public class ZoomType
```

Возможные значения размера документа, отображаемого на экране в Microsoft Word.
## Поля

| Поле | Описание |
| --- | --- |
| [CUSTOM](#CUSTOM) | Процент увеличения задается явно. |
| [FULL_PAGE](#FULL-PAGE) | Процент увеличения автоматически пересчитывается, чтобы уместиться на одной полной странице. |
| [NONE](#NONE) | Указывает на использование явного процента масштабирования. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Процент увеличения автоматически пересчитывается в соответствии с шириной страницы. |
| [TEXT_FIT](#TEXT-FIT) | Процент увеличения автоматически пересчитывается, чтобы соответствовать тексту. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String zoomTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int zoomType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int zoomType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Процент увеличения задается явно. Он не пересчитывается автоматически при изменении размера элемента управления.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Процент увеличения автоматически пересчитывается, чтобы уместиться на одной полной странице.

### NONE {#NONE}
```
public static int NONE
```


 Указывает на использование явного процента масштабирования. Такой же как[CUSTOM](../../com.aspose.words/zoomtype\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Процент увеличения автоматически пересчитывается в соответствии с шириной страницы.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Процент увеличения автоматически пересчитывается, чтобы соответствовать тексту.

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
### fromName(String zoomTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String zoomTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int zoomType) {#getName-int-}
```
public static String getName(int zoomType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| zoomType | int |  |

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
### toString(int zoomType) {#toString-int-}
```
public static String toString(int zoomType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| zoomType | int |  |

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
