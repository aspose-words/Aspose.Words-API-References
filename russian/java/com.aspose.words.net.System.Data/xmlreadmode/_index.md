---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как считывать XML‑данные и реляционную схему в DataSet на Java."
type: docs
weight: 37
url: /ru/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

Указывает, как считывать XML‑данные и реляционную схему в [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | По умолчанию. |
| [DIFF_GRAM](#DIFF-GRAM) | Читает DiffGram, применяя изменения из DiffGram к [DataSet](../../com.aspose.words.net.system.data/dataset/) и сохраняя значения [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState). |
| [FRAGMENT](#FRAGMENT) | Читает фрагменты XML, такие как генерируемые при выполнении запросов FOR XML, относительно экземпляра SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | Игнорирует любую встроенную схему и считывает данные в существующую схему [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [INFER_SCHEMA](#INFER-SCHEMA) | Игнорирует любую встроенную схему, выводит схему из данных и загружает данные. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Игнорирует любую встроенную схему, выводит строго типизированную схему из данных и загружает данные. |
| [READ_SCHEMA](#READ-SCHEMA) | Читает любую встроенную схему и загружает данные. |
## Методы

| Метод | Описание |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


По умолчанию.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


Читает DiffGram, применяя изменения из DiffGram к [DataSet](../../com.aspose.words.net.system.data/dataset/) и сохраняя значения [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState).

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


Читает XML‑фрагменты, такие как те, которые генерируются при выполнении запросов FOR XML, относительно экземпляра SQL Server. Когда [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) установлен в значение Fragment, пространство имён по умолчанию читается как встроенная схема.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


Игнорирует любую встроенную схему и читает данные в существующую схему [DataSet](../../com.aspose.words.net.system.data/dataset/). Если какие‑либо данные не соответствуют существующей схеме, они отбрасываются (включая данные из разных пространств имён, определённых для [DataSet](../../com.aspose.words.net.system.data/dataset/)). Если данные представлены в виде DiffGram, IgnoreSchema имеет ту же функциональность, что и DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


Игнорирует любую встроенную схему, выводит схему из данных и загружает их. Если [DataSet](../../com.aspose.words.net.system.data/dataset/) уже содержит схему, текущая схема расширяется добавлением новых таблиц или добавлением столбцов к существующим таблицам. Исключение генерируется, если выводимая таблица уже существует, но в другом пространстве имён, или если какие‑либо выводимые столбцы конфликтуют с существующими столбцами.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


Игнорирует любую встроенную схему, выводит строго типизированную схему из данных и загружает их. Если тип нельзя вывести из данных, он интерпретируется как строковые данные. Если [DataSet](../../com.aspose.words.net.system.data/dataset/) уже содержит схему, текущая схема расширяется либо добавлением новых таблиц, либо добавлением столбцов к существующим таблицам. Исключение генерируется, если выводимая таблица уже существует, но в другом пространстве имён, или если какие‑либо выводимые столбцы конфликтуют с существующими столбцами.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


Читает любую встроенную схему и загружает данные. Если [DataSet](../../com.aspose.words.net.system.data/dataset/) уже содержит схему, в неё могут быть добавлены новые таблицы, но исключение генерируется, если какие‑либо таблицы во встроенной схеме уже существуют в [DataSet](../../com.aspose.words.net.system.data/dataset/).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
