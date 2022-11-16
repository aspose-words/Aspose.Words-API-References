---
title: ResourceLoadingAction
second_title: Справочник по API Aspose.Words для Java
description: Задает режим загрузки ресурсов.
type: docs
weight: 479
url: /ru/java/com.aspose.words/resourceloadingaction/
---

**Наследование:**
java.lang.Object
```
public class ResourceLoadingAction
```

Задает режим загрузки ресурсов.

 Чтобы узнать больше, посетите**Specify Load Options** документальная статья.
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Aspose.Words загрузит этот ресурс как обычно. |
| [SKIP](#SKIP) | Aspose.Words пропустит загрузку этого ресурса. |
| [USER_PROVIDED](#USER-PROVIDED) |  Aspose.Words будет использовать массив байтов, предоставленный пользователем в[ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs\#setData-byte---) как ресурсные данные. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String resourceLoadingActionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int resourceLoadingAction)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int resourceLoadingAction)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aspose.Words загрузит этот ресурс как обычно.

### SKIP {#SKIP}
```
public static int SKIP
```


Aspose.Words пропустит загрузку этого ресурса. Для изображения будет храниться только ссылка без данных, таблица стилей CSS будет игнорироваться для формата HTML.

### USER_PROVIDED {#USER-PROVIDED}
```
public static int USER_PROVIDED
```


 Aspose.Words будет использовать массив байтов, предоставленный пользователем в[ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs\#setData-byte---) как ресурсные данные.

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
### fromName(String resourceLoadingActionName) {#fromName-java.lang.String-}
```
public static int fromName(String resourceLoadingActionName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| resourceLoadingActionName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int resourceLoadingAction) {#getName-int-}
```
public static String getName(int resourceLoadingAction)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| resourceLoadingAction | int |  |

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
### toString(int resourceLoadingAction) {#toString-int-}
```
public static String toString(int resourceLoadingAction)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| resourceLoadingAction | int |  |

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
