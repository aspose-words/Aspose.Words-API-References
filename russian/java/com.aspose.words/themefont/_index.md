---
title: ThemeFont
second_title: Справочник по API Aspose.Words для Java
description: Указывает типы имен шрифтов темы для тем документа.
type: docs
weight: 576
url: /ru/java/com.aspose.words/themefont/
---

**Наследование:**
java.lang.Object
```
public class ThemeFont
```

Указывает типы имен шрифтов темы для тем документа. Указывает тип шрифта темы, на который можно ссылаться как на шрифт темы в свойствах родительского объекта. Этот шрифт темы является ссылкой на один из предопределенных шрифтов темы, расположенный в части документа «Тема», что позволяет централизованно задавать информацию о шрифте в документе.
## Поля

| Поле | Описание |
| --- | --- |
| [MAJOR](#MAJOR) | Основной тематический шрифт. |
| [MINOR](#MINOR) | Незначительный шрифт темы. |
| [NONE](#NONE) | Нет шрифта темы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String themeFontName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int themeFont)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int themeFont)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### MAJOR {#MAJOR}
```
public static int MAJOR
```


Основной тематический шрифт.

### MINOR {#MINOR}
```
public static int MINOR
```


Незначительный шрифт темы.

### NONE {#NONE}
```
public static int NONE
```


Нет шрифта темы.

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
### fromName(String themeFontName) {#fromName-java.lang.String-}
```
public static int fromName(String themeFontName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| themeFontName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int themeFont) {#getName-int-}
```
public static String getName(int themeFont)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| themeFont | int |  |

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
### toString(int themeFont) {#toString-int-}
```
public static String toString(int themeFont)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| themeFont | int |  |

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
