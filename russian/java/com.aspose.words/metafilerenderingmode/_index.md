---
title: MetafileRenderingMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF.
type: docs
weight: 396
url: /ru/java/com.aspose.words/metafilerenderingmode/
---

**Наследование:**
java.lang.Object
```
public class MetafileRenderingMode
```

Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF.
## Поля

| Поле | Описание |
| --- | --- |
| [BITMAP](#BITMAP) | Aspose.Words вызывает GDI+ для преобразования метафайла в растровое изображение, а затем сохраняет растровое изображение в выходной документ. |
| [VECTOR](#VECTOR) | Aspose.Words отображает метафайл как векторную графику. |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words пытается отобразить метафайл как векторную графику. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int metafileRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int metafileRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words вызывает GDI+ для преобразования метафайла в растровое изображение, а затем сохраняет растровое изображение в выходной документ.

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words отображает метафайл как векторную графику.

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words пытается отобразить метафайл как векторную графику. Если Aspose.Words не может правильно преобразовать некоторые записи метафайла в векторную графику, Aspose.Words преобразует этот метафайл в растровое изображение.

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
### fromName(String metafileRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String metafileRenderingModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int metafileRenderingMode) {#getName-int-}
```
public static String getName(int metafileRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| metafileRenderingMode | int |  |

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
### toString(int metafileRenderingMode) {#toString-int-}
```
public static String toString(int metafileRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| metafileRenderingMode | int |  |

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
