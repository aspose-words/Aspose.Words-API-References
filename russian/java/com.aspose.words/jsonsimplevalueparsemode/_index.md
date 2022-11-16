---
title: JsonSimpleValueParseMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает режим анализа простых значений JSON null boolean number integer и string при загрузке JSON.
type: docs
weight: 355
url: /ru/java/com.aspose.words/jsonsimplevalueparsemode/
---

**Наследование:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Указывает режим анализа простых значений JSON (пустых, логических, числовых, целых и строковых) при загрузке JSON. Такой режим не влияет на синтаксический анализ значений даты и времени.
## Поля

| Поле | Описание |
| --- | --- |
| [LOOSE](#LOOSE) | Указывает режим, в котором типы простых значений JSON определяются при разборе их строковых представлений. |
| [STRICT](#STRICT) | Указывает режим, в котором типы простых значений JSON определяются из самой нотации JSON. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Указывает режим, в котором типы простых значений JSON определяются при разборе их строковых представлений. Например, тип «prop» из фрагмента JSON «\ { реквизит: "123"\}' в этом режиме определяется как целое число.

### STRICT {#STRICT}
```
public static int STRICT
```


Указывает режим, в котором типы простых значений JSON определяются из самой нотации JSON. Например, тип «prop» из фрагмента JSON «\ { реквизит: "123"\}' определяется как строка в этом режиме.

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
### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String-}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int jsonSimpleValueParseMode) {#getName-int-}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

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
### toString(int jsonSimpleValueParseMode) {#toString-int-}
```
public static String toString(int jsonSimpleValueParseMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

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
