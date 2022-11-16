---
title: CssStyleSheetType
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как стили каскадной таблицы стилей CSS экспортируются в HTML.
type: docs
weight: 97
url: /ru/java/com.aspose.words/cssstylesheettype/
---

**Наследование:**
java.lang.Object
```
public class CssStyleSheetType
```

Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML.
## Поля

| Поле | Описание |
| --- | --- |
| [EMBEDDED](#EMBEDDED) | Стили CSS записываются отдельно от содержимого в таблице стилей, встроенной в файл HTML. |
| [EXTERNAL](#EXTERNAL) | Стили CSS записываются отдельно от содержимого таблицы стилей во внешнем файле. |
| [INLINE](#INLINE) |  Стили CSS записываются встроенными (как значение**style** атрибут каждого элемента). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int cssStyleSheetType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int cssStyleSheetType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


Стили CSS записываются отдельно от содержимого в таблице стилей, встроенной в файл HTML.

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


Стили CSS записываются отдельно от содержимого таблицы стилей во внешнем файле. Файл HTML связывает таблицу стилей.

### INLINE {#INLINE}
```
public static int INLINE
```


 Стили CSS записываются встроенными (как значение**style** атрибут каждого элемента).

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
### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String cssStyleSheetTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int cssStyleSheetType) {#getName-int-}
```
public static String getName(int cssStyleSheetType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| cssStyleSheetType | int |  |

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
### toString(int cssStyleSheetType) {#toString-int-}
```
public static String toString(int cssStyleSheetType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| cssStyleSheetType | int |  |

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
