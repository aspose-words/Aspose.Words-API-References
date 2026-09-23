---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words для Java"
description: "Представляет кэш данных в памяти в Java."
type: docs
weight: 24
url: /ru/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Представляет кэш данных в памяти.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataSet()](#DataSet) | Инициализирует новый экземпляр класса [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | Инициализирует новый экземпляр класса DataSet с данными, полученными из Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | Инициализирует новый экземпляр класса DataSet с данными, полученными из Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Инициализирует новый экземпляр класса [DataSet](../../com.aspose.words.net.system.data/dataset/) с указанным именем. |
## Методы

| Метод | Описание |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | Очищает [DataSet](../../com.aspose.words.net.system.data/dataset/) от всех данных, удаляя все строки во всех таблицах. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Получает имя текущего [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getEnforceConstraints()](#getEnforceConstraints) | Получает значение, указывающее, соблюдаются ли правила ограничений при попытке любой операции обновления. |
| [getNamespace()](#getNamespace) | Получает пространство имён [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getRelations()](#getRelations) | Получить коллекцию связей, которые связывают таблицы и позволяют навигацию от родительских таблиц к дочерним. |
| [getTables()](#getTables) | Получает коллекцию таблиц, содержащихся в [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Читает схему XML и данные в [DataSet](../../com.aspose.words.net.system.data/dataset/) с использованием указанного java.io.InputStream. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Читает схему XML и данные в DataSet с использованием указанного java.io.InputStream и [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXml(String fileName)](#readXml-java.lang.String) | Читает схему XML и данные в [DataSet](../../com.aspose.words.net.system.data/dataset/) с использованием указанного файла. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Читает схему XML и данные в DataSet с использованием указанного файла и [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Читает схему XML из указанного java.io.InputStream в [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Читает схему XML из указанного файла в [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [reset()](#reset) | Сбрасывает [DataSet](../../com.aspose.words.net.system.data/dataset/) в исходное состояние. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Устанавливает имя текущего [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Устанавливает значение, указывающее, соблюдаются ли правила ограничений при попытке любой операции обновления. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Устанавливает информацию о локали, используемую для сравнения строк в таблице. |
### DataSet() {#DataSet}
```
public DataSet()
```


Инициализирует новый экземпляр класса [DataSet](../../com.aspose.words.net.system.data/dataset/).

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


Инициализирует новый экземпляр класса DataSet с данными, полученными из Connection. Таблицы, связи, ограничения и индексы будут скопированы в DataSet.

По умолчанию имя схемы не будет использоваться.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| connection | java.sql.Connection | которая содержит данные БД. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


Инициализирует новый экземпляр класса DataSet с данными, полученными из Connection. Таблицы, связи, ограничения и индексы будут скопированы в DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

или

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| connection | java.sql.Connection | которая содержит данные БД. |
| schemaName | java.lang.String | которая содержит таблицы для импорта. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Инициализирует новый экземпляр класса [DataSet](../../com.aspose.words.net.system.data/dataset/) с указанным именем.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSetName | java.lang.String | Имя [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean - true, если схема была прочитана
### clear() {#clear}
```
public void clear()
```


Очищает [DataSet](../../com.aspose.words.net.system.data/dataset/) от всех данных, удаляя все строки во всех таблицах.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Получает имя текущего [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - Имя [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Получает значение, указывающее, соблюдаются ли правила ограничений при попытке любой операции обновления.

**Returns:**
boolean - true, если правила применяются; иначе false. По умолчанию true.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Получает пространство имён [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - Пространство имён [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Получить коллекцию связей, которые связывают таблицы и позволяют навигацию от родительских таблиц к дочерним.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


Получает коллекцию таблиц, содержащихся в [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean - true, если локаль была установлена
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Читает схему XML и данные в [DataSet](../../com.aspose.words.net.system.data/dataset/) с использованием указанного java.io.InputStream.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream | Объект, производный от java.io.InputStream. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Читает схему XML и данные в DataSet с использованием указанного java.io.InputStream и [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream | Поток, из которого читать. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | Одно из значений [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Читает схему XML и данные в [DataSet](../../com.aspose.words.net.system.data/dataset/) с использованием указанного файла.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла (включая путь), из которого читать. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Читает схему XML и данные в DataSet с использованием указанного файла и [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | указанный файл |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Читает схему XML из указанного java.io.InputStream в [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream | java.io.InputStream, из которого читать. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Читает схему XML из указанного файла в [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла (включая путь), из которого читать. |

### reset() {#reset}
```
public void reset()
```


Сбрасывает [DataSet](../../com.aspose.words.net.system.data/dataset/) до его исходного состояния. Подклассы должны переопределить [reset()](../../com.aspose.words.net.system.data/dataset/\#reset), чтобы восстановить [DataSet](../../com.aspose.words.net.system.data/dataset/) до его исходного состояния.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Устанавливает имя текущего [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Устанавливает значение, указывающее, соблюдаются ли правила ограничений при попытке любой операции обновления.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | true, если правила применяются; иначе false. По умолчанию true. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Устанавливает информацию о локали, используемую для сравнения строк в таблице.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| locale | java.util.Locale | этого набора данных |

