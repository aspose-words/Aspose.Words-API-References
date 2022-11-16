---
title: XmlReadMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как считывать XML-данные и реляционную схему в файл .
type: docs
weight: 37
url: /ru/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Наследование:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

 Указывает, как считывать XML-данные и реляционную схему в[DataSet](../../com.aspose.words.net.system.data/dataset).
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | По умолчанию. |
| [DIFF_GRAM](#DIFF-GRAM) |  Читает DiffGram, применяя изменения из DiffGram к[DataSet](../../com.aspose.words.net.system.data/dataset) и сохранение[DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow\#getRowState--) ценности. |
| [FRAGMENT](#FRAGMENT) | Считывает фрагменты XML, например созданные при выполнении запросов FOR XML, относительно экземпляра SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) |  Игнорирует любую встроенную схему и считывает данные в существующую[DataSet](../../com.aspose.words.net.system.data/dataset) схема. |
| [INFER_SCHEMA](#INFER-SCHEMA) | Игнорирует любую встроенную схему, выводит схему из данных и загружает данные. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Игнорирует любую встроенную схему, выводит строго типизированную схему из данных и загружает данные. |
| [READ_SCHEMA](#READ-SCHEMA) | Читает любую встроенную схему и загружает данные. |
## Методы

| Метод | Описание |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String-) |  |
| [compareTo(E arg0)](#compareTo-E-) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDeclaringClass()](#getDeclaringClass--) |  |
| [hashCode()](#hashCode--) |  |
| [name()](#name--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [ordinal()](#ordinal--) |  |
| [toString()](#toString--) |  |
| [valueOf(String name)](#valueOf-java.lang.String-) |  |
| [values()](#values--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


По умолчанию.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


 Читает DiffGram, применяя изменения из DiffGram к[DataSet](../../com.aspose.words.net.system.data/dataset) и сохранение[DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow\#getRowState--) ценности.

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


 Считывает фрагменты XML, например созданные при выполнении запросов FOR XML, относительно экземпляра SQL Server. Когда[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) установлено значение Fragment, пространство имен по умолчанию читается как встроенная схема.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


 Игнорирует любую встроенную схему и считывает данные в существующую[DataSet](../../com.aspose.words.net.system.data/dataset)схема. Если какие-либо данные не соответствуют существующей схеме, они отбрасываются (включая данные из разных пространств имен, определенных для[DataSet](../../com.aspose.words.net.system.data/dataset)). Если данные представляют собой DiffGram, IgnoreSchema имеет те же функции, что и DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


 Игнорирует любую встроенную схему, выводит схему из данных и загружает данные. Если[DataSet](../../com.aspose.words.net.system.data/dataset) уже содержит схему, текущая схема расширяется путем добавления новых таблиц или добавления столбцов в существующие таблицы. Исключение создается, если выводимая таблица уже существует, но с другим пространством имен, или если какой-либо из выводимых столбцов конфликтует с существующими столбцами.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


 Игнорирует любую встроенную схему, выводит строго типизированную схему из данных и загружает данные. Если тип не может быть выведен из данных, он интерпретируется как строковые данные. Если[DataSet](../../com.aspose.words.net.system.data/dataset)уже содержит схему, текущая схема расширяется либо путем добавления новых таблиц, либо путем добавления столбцов в существующие таблицы. Исключение создается, если выводимая таблица уже существует, но с другим пространством имен, или если какой-либо из выводимых столбцов конфликтует с существующими столбцами.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


 Читает любую встроенную схему и загружает данные. Если[DataSet](../../com.aspose.words.net.system.data/dataset) уже содержит схему, в схему могут быть добавлены новые таблицы, но возникает исключение, если какие-либо таблицы во встроенной схеме уже существуют в[DataSet](../../com.aspose.words.net.system.data/dataset).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String-}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Возвращает:**
Т
### compareTo(E arg0) {#compareTo-E-}
```
public final int compareTo(E arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | E |  |

**Возвращает:**
инт
### equals(Object arg0) {#equals-java.lang.Object-}
```
public final boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDeclaringClass() {#getDeclaringClass--}
```
public final Class<E> getDeclaringClass()
```




**Возвращает:**
java.lang.Класс<E>
### hashCode() {#hashCode--}
```
public final int hashCode()
```




**Возвращает:**
инт
### name() {#name--}
```
public final String name()
```




**Возвращает:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### ordinal() {#ordinal--}
```
public final int ordinal()
```




**Возвращает:**
инт
### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String-}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |

**Возвращает:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)
### values() {#values--}
```
public static System.Data.XmlReadMode[] values()
```




**Возвращает:**
com.aspose.words.net.System.Data.XmlReadMode[]
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
