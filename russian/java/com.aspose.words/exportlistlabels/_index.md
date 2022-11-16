---
title: ExportListLabels
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как метки списков экспортируются в HTML, MHTML и EPUB.
type: docs
weight: 150
url: /ru/java/com.aspose.words/exportlistlabels/
---

**Наследование:**
java.lang.Object
```
public class ExportListLabels
```

Указывает, как метки списков экспортируются в форматы HTML, MHTML и EPUB.
## Поля

| Поле | Описание |
| --- | --- |
| [AS_INLINE_TEXT](#AS-INLINE-TEXT) | Выводит все метки списка как встроенный текст. |
| [AUTO](#AUTO) | Выводит метки списка в автоматическом режиме. |
| [BY_HTML_TAGS](#BY-HTML-TAGS) | Выводит все метки списка как собственные элементы HTML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String exportListLabelsName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int exportListLabels)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int exportListLabels)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AS_INLINE_TEXT {#AS-INLINE-TEXT}
```
public static int AS_INLINE_TEXT
```


Выводит все метки списка как встроенный текст. HTML

Тег используется для любого представления метки списка.

### AUTO {#AUTO}
```
public static int AUTO
```


Выводит метки списка в автоматическом режиме. По возможности использует собственные элементы HTML. HTML

 *  теги используются для представления метки списка, если это не приводит к потере форматирования, в противном случае HTML
    
    тег используется.

### BY_HTML_TAGS {#BY-HTML-TAGS}
```
public static int BY_HTML_TAGS
```


Выводит все метки списка как собственные элементы HTML. HTML

 *  теги используются для представления метки списка. Возможна некоторая потеря форматирования.

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
### fromName(String exportListLabelsName) {#fromName-java.lang.String-}
```
public static int fromName(String exportListLabelsName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| exportListLabelsName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int exportListLabels) {#getName-int-}
```
public static String getName(int exportListLabels)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| exportListLabels | int |  |

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
### toString(int exportListLabels) {#toString-int-}
```
public static String toString(int exportListLabels)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| exportListLabels | int |  |

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
