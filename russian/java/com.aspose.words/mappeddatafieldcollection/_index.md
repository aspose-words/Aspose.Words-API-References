---
title: MappedDataFieldCollection
second_title: Справочник по API Aspose.Words для Java
description: Позволяет автоматически сопоставлять имена полей в вашем источнике данных и имена полей слияния в документе.
type: docs
weight: 387
url: /ru/java/com.aspose.words/mappeddatafieldcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

Позволяет автоматически сопоставлять имена полей в вашем источнике данных и имена полей слияния в документе.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

Это реализовано как набор строковых ключей в строковые значения. Ключи — это имена полей слияния в документе, а значения — это имена полей в вашем источнике данных.
## Методы

| Метод | Описание |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String-) | Добавляет новое сопоставление полей. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String-) | Определяет, существует ли в коллекции сопоставление из указанного поля в документе. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String-) | Определяет, существует ли в коллекции сопоставление из указанного поля в источнике данных. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String documentFieldName)](#get-java.lang.String-) | Получает имя поля в источнике данных, связанном с указанным полем слияния. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект итератора словаря, который можно использовать для перебора всех элементов в коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String documentFieldName)](#remove-java.lang.String-) | Удаляет сопоставление полей. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String-) | Задает имя поля в источнике данных, связанного с указанным полем слияния. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String-}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Добавляет новое сопоставление полей.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String | Регистрозависимое имя поля слияния в документе. |
| dataSourceFieldName | java.lang.String | Регистрозависимое имя поля в источнике данных. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### containsKey(String documentFieldName) {#containsKey-java.lang.String-}
```
public boolean containsKey(String documentFieldName)
```


Определяет, существует ли в коллекции сопоставление из указанного поля в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String | Регистрозависимое имя поля слияния в документе. |

**Возвращает:**
boolean - Истинно, если элемент найден в коллекции; в противном случае ложно.
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String-}
```
public boolean containsValue(String dataSourceFieldName)
```


Определяет, существует ли в коллекции сопоставление из указанного поля в источнике данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Регистрозависимое имя поля в источнике данных. |

**Возвращает:**
boolean - Истинно, если элемент найден в коллекции; в противном случае ложно.
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
### get(String documentFieldName) {#get-java.lang.String-}
```
public String get(String documentFieldName)
```


Получает имя поля в источнике данных, связанном с указанным полем слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**Возвращает:**
java.lang.String — имя поля в источнике данных, связанного с указанным полем слияния.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

**Возвращает:**
int - количество элементов, содержащихся в коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект итератора словаря, который можно использовать для перебора всех элементов в коллекции.

**Возвращает:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(String documentFieldName) {#remove-java.lang.String-}
```
public void remove(String documentFieldName)
```


Удаляет сопоставление полей.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String | Регистрозависимое имя поля слияния в документе. |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String documentFieldName, String value)
```


Задает имя поля в источнике данных, связанного с указанным полем слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| value | java.lang.String | Имя поля в источнике данных, связанного с указанным полем слияния. |

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
