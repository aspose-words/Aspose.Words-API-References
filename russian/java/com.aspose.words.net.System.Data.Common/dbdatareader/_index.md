---
title: DbDataReader
second_title: Справочник по API Aspose.Words для Java
description: Считывает прямой поток строк из источника данных.
type: docs
weight: 10
url: /ru/java/com.aspose.words.net.system.data.common/dbdatareader/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
[com.aspose.words.net.System.Data.IDataReader](../../com.aspose.words.net.system.data/idatareader), [com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord), java.lang.Итерабельный
```
public abstract class DbDataReader implements System.Data.IDataReader, System.Data.IDataRecord, Iterable
```

Считывает прямой поток строк из источника данных.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DbDataReader()](#DbDataReader--) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String columnName)](#get-java.lang.String-) | Этот метод принадлежит IDataRecord в .NET. |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DbDataReader() {#DbDataReader--}
```
public DbDataReader()
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
### get(String columnName) {#get-java.lang.String-}
```
public abstract Object get(String columnName)
```


Этот метод принадлежит IDataRecord в .NET.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Возвращает:**
java.lang.Объект
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
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
