---
title: DataSet
second_title: Справочник по API Aspose.Words для Java
description: Представляет кэш данных в памяти.
type: docs
weight: 24
url: /ru/java/com.aspose.words.net.system.data/dataset/
---

**Наследование:**
java.lang.Object
```
public class DataSet
```

Представляет кэш данных в памяти.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataSet()](#DataSet--) |  Инициализирует новый экземпляр[DataSet](../../com.aspose.words.net.system.data/dataset) учебный класс. |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection-) | Инициализирует новый экземпляр класса DataSet данными, взятыми из Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String-) | Инициализирует новый экземпляр класса DataSet данными, взятыми из Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String-) |  Инициализирует новый экземпляр[DataSet](../../com.aspose.words.net.system.data/dataset) класс с заданным именем. |
## Методы

| Метод | Описание |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead--) |  |
| [clear()](#clear--) |  Очищает[DataSet](../../com.aspose.words.net.system.data/dataset) любых данных, удалив все строки во всех таблицах. |
| [close()](#close--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDataSetName()](#getDataSetName--) |  Получает имя текущего[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [getEnforceConstraints()](#getEnforceConstraints--) | Получает значение, указывающее, соблюдаются ли правила ограничения при попытке выполнения любой операции обновления. |
| [getNamespace()](#getNamespace--) |  Получает пространство имен[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [getRelations()](#getRelations--) | Получите коллекцию отношений, которые связывают таблицы и позволяют переходить от родительских таблиц к дочерним. |
| [getTables()](#getTables--) |  Получает коллекцию таблиц, содержащихся в[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [hashCode()](#hashCode--) |  |
| [isLocaleSpecified()](#isLocaleSpecified--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream-) |  Считывает XML-схему и данные в[DataSet](../../com.aspose.words.net.system.data/dataset) используя указанный java.io.InputStream. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode-) |  Считывает XML-схему и данные в DataSet, используя указанный java.io.InputStream и[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode). |
| [readXml(String fileName)](#readXml-java.lang.String-) |  Считывает XML-схему и данные в[DataSet](../../com.aspose.words.net.system.data/dataset) используя указанный файл. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode-) | Считывает XML-схему и данные в DataSet, используя указанный файл и[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream-) |  Считывает XML-схему из указанного java.io.InputStream в[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String-) |  Считывает XML-схему из указанного файла в[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [reset()](#reset--) |  Сбрасывает[DataSet](../../com.aspose.words.net.system.data/dataset) в исходное состояние. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String-) |  Устанавливает имя текущего[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean-) | Задает значение, указывающее, соблюдаются ли правила ограничения при попытке выполнения любой операции обновления. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale-) | Задает информацию о локали, используемую для сравнения строк в таблице. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataSet() {#DataSet--}
```
public DataSet()
```


 Инициализирует новый экземпляр[DataSet](../../com.aspose.words.net.system.data/dataset) учебный класс.

### DataSet(Connection connection) {#DataSet-java.sql.Connection-}
```
public DataSet(Connection connection)
```


Инициализирует новый экземпляр класса DataSet данными, взятыми из Connection. Таблицы, отношения, ограничения и индексы будут скопированы в DataSet.

По умолчанию имя схемы не используется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| connection | java.sql.Connection | который содержит данные БД. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String-}
```
public DataSet(Connection connection, String schemaName)
```


Инициализирует новый экземпляр класса DataSet данными, взятыми из Connection. Таблицы, отношения, ограничения и индексы будут скопированы в DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

или же

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| connection | java.sql.Connection | который содержит данные БД. |
| schemaName | java.lang.String | который содержит таблицы для импорта. |

### DataSet(String dataSetName) {#DataSet-java.lang.String-}
```
public DataSet(String dataSetName)
```


 Инициализирует новый экземпляр[DataSet](../../com.aspose.words.net.system.data/dataset) класс с заданным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSetName | java.lang.String |  Имя[DataSet](../../com.aspose.words.net.system.data/dataset). |

### IsSchemaWasRead() {#IsSchemaWasRead--}
```
public boolean IsSchemaWasRead()
```




**Возвращает:**
boolean - истина, если схема была прочитана
### clear() {#clear--}
```
public void clear()
```


 Очищает[DataSet](../../com.aspose.words.net.system.data/dataset) любых данных, удалив все строки во всех таблицах.

### close() {#close--}
```
public void close()
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDataSetName() {#getDataSetName--}
```
public String getDataSetName()
```


 Получает имя текущего[DataSet](../../com.aspose.words.net.system.data/dataset).

**Возвращает:**
 java.lang.String — Имя[DataSet](../../com.aspose.words.net.system.data/dataset).
### getEnforceConstraints() {#getEnforceConstraints--}
```
public boolean getEnforceConstraints()
```


Получает значение, указывающее, соблюдаются ли правила ограничения при попытке выполнения любой операции обновления.

**Возвращает:**
boolean - true, если правила применяются; иначе ложно. Значение по умолчанию верно.
### getNamespace() {#getNamespace--}
```
public String getNamespace()
```


 Получает пространство имен[DataSet](../../com.aspose.words.net.system.data/dataset).

**Возвращает:**
 java.lang.String — пространство имен[DataSet](../../com.aspose.words.net.system.data/dataset).
### getRelations() {#getRelations--}
```
public System.Data.DataRelationCollection getRelations()
```


Получите коллекцию отношений, которые связывают таблицы и позволяют переходить от родительских таблиц к дочерним.

**Возвращает:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - А[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) который содержит коллекцию[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты. Пустая коллекция возвращается, если нет[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты существуют.
### getTables() {#getTables--}
```
public System.Data.DataTableCollection getTables()
```


 Получает коллекцию таблиц, содержащихся в[DataSet](../../com.aspose.words.net.system.data/dataset).

**Возвращает:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection) -[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection)содержится в этом[DataSet](../../com.aspose.words.net.system.data/dataset) . Пустая коллекция возвращается, если нет[DataTable](../../com.aspose.words.net.system.data/datatable) объекты существуют.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isLocaleSpecified() {#isLocaleSpecified--}
```
public boolean isLocaleSpecified()
```




**Возвращает:**
boolean - true, если локаль была установлена
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### readXml(InputStream stream) {#readXml-java.io.InputStream-}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


 Считывает XML-схему и данные в[DataSet](../../com.aspose.words.net.system.data/dataset) используя указанный java.io.InputStream.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream | Объект, производный от java.io.InputStream. |

**Возвращает:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) -[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) используется для чтения данных. Возвращаемое значение является одним из[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) константы.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode-}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


 Считывает XML-схему и данные в DataSet, используя указанный java.io.InputStream и[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream | Поток, из которого нужно читать. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) |  Один из[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) ценности. |

**Возвращает:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) - XmlReadMode, используемый для чтения данных.
### readXml(String fileName) {#readXml-java.lang.String-}
```
public System.Data.XmlReadMode readXml(String fileName)
```


 Считывает XML-схему и данные в[DataSet](../../com.aspose.words.net.system.data/dataset) используя указанный файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла (включая путь), из которого следует читать. |

**Возвращает:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) - XmlReadMode, используемый для чтения данных. Возвращаемое значение является одним из[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) константы.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode-}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Считывает XML-схему и данные в DataSet, используя указанный файл и[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | указанный файл |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) | \{[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) |

**Возвращает:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) - режим, который использовался при чтении
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream-}
```
public void readXmlSchema(InputStream stream)
```


 Считывает XML-схему из указанного java.io.InputStream в[DataSet](../../com.aspose.words.net.system.data/dataset).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream | java.io.InputStream, из которого следует читать. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String-}
```
public void readXmlSchema(String fileName)
```


 Считывает XML-схему из указанного файла в[DataSet](../../com.aspose.words.net.system.data/dataset).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла (включая путь), из которого следует читать. |

### reset() {#reset--}
```
public void reset()
```


 Сбрасывает[DataSet](../../com.aspose.words.net.system.data/dataset) в исходное состояние. Подклассы должны переопределять[reset()](../../com.aspose.words.net.system.data/dataset\#reset--) восстановить[DataSet](../../com.aspose.words.net.system.data/dataset) в исходное состояние.

### setDataSetName(String value) {#setDataSetName-java.lang.String-}
```
public void setDataSetName(String value)
```


 Устанавливает имя текущего[DataSet](../../com.aspose.words.net.system.data/dataset).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Имя[DataSet](../../com.aspose.words.net.system.data/dataset). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean-}
```
public void setEnforceConstraints(boolean value)
```


Задает значение, указывающее, соблюдаются ли правила ограничения при попытке выполнения любой операции обновления.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | true, если правила применяются; иначе ложно. Значение по умолчанию верно. |

### setLocale(Locale locale) {#setLocale-java.util.Locale-}
```
public void setLocale(Locale locale)
```


Задает информацию о локали, используемую для сравнения строк в таблице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| locale | java.util.Locale | этого набора данных |

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
