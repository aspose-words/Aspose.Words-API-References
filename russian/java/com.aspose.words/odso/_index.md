---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words для Java"
description: "Указывает настройки Office Data Source Object ODSO для источника данных слияния писем в Java."
type: docs
weight: 487
url: /ru/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Указывает настройки Office Data Source Object (ODSO) для источника данных слияния писем.

Чтобы узнать больше, посетите статью документации [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

ODSO, по-видимому, является "new" способом, который более новые версии Microsoft Word предпочитают использовать при указании определённых типов источников данных для документа слияния писем. ODSO, вероятно, впервые появился в Microsoft Word 2000.

Использование ODSO плохо документировано, и лучший способ узнать, как использовать свойства этого объекта, — создать документ с нужным источником данных вручную в Microsoft Word, а затем открыть этот документ с помощью Aspose.Words и изучить свойства объектов [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) и [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). Это хороший подход, если вы хотите научиться программно настраивать источник данных, например.

Обычно вам не нужно создавать объекты этого класса напрямую, потому что настройки ODSO всегда доступны через свойство [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone) | Возвращает глубокую копию этого объекта. |
| [getColumnDelimiter()](#getColumnDelimiter) | Указывает символ, который будет интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. |
| [getDataSource()](#getDataSource) | Указывает расположение внешнего источника данных, который будет подключён к документу для выполнения слияния писем. |
| [getDataSourceType()](#getDataSourceType) | Указывает тип внешнего источника данных, который будет подключён в рамках информации о соединении ODSO для этого слияния писем. |
| [getFieldMapDatas()](#getFieldMapDatas) | Возвращает коллекцию объектов, определяющих, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Указывает, что хост‑приложение должно рассматривать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена всех столбцов источника. |
| [getRecipientDatas()](#getRecipientDatas) | Возвращает коллекцию объектов, определяющих включение/исключение отдельных записей в слиянии писем. |
| [getTableName()](#getTableName) | Указывает конкретный набор данных, к которому источник должен быть подключён во внешнем источнике данных. |
| [getUdlConnectString()](#getUdlConnectString) | Указывает строку подключения Universal Data Link (UDL), используемую для подключения к внешнему источнику данных. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Указывает символ, который будет интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Указывает расположение внешнего источника данных, который будет подключён к документу для выполнения слияния писем. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Указывает тип внешнего источника данных, который будет подключён в рамках информации о соединении ODSO для этого слияния писем. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Устанавливает коллекцию объектов, определяющих, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Указывает, что хост‑приложение должно рассматривать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена всех столбцов источника. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Устанавливает коллекцию объектов, определяющих включение/исключение отдельных записей в слиянии писем. |
| [setTableName(String value)](#setTableName-java.lang.String) | Указывает конкретный набор данных, к которому источник должен быть подключён во внешнем источнике данных. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Указывает строку подключения Universal Data Link (UDL), используемую для подключения к внешнему источнику данных. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Возвращает глубокую копию этого объекта.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Указывает символ, который будет интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию — 0, что означает отсутствие определённого разделителя столбцов.

 **Remarks:** 

RK, я никогда не видел, чтобы это использовалось.

**Returns:**
char — соответствующее значение  char .
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Указывает расположение внешнего источника данных, который будет подключён к документу для выполнения слияния писем. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Указывает тип внешнего источника данных, который будет подключён в рамках информации о соединении ODSO для этого слияния писем. Значение по умолчанию — [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Эта настройка представляет собой лишь рекомендацию типа источника данных, используемого для этого слияния писем.

**Returns:**
int — соответствующее значение  int . Возвращаемое значение является одной из констант [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/).
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Возвращает коллекцию объектов, определяющих, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. Этот объект никогда не является  null .

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Указывает, что хост‑приложение должно рассматривать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена всех столбцов источника. Значение по умолчанию —  false .

 **Remarks:** 

RK, я никогда не видел, чтобы это использовалось.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Возвращает коллекцию объектов, определяющих включение/исключение отдельных записей в слиянии писем. Этот объект никогда не является  null .

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Указывает конкретный набор данных, к которому источник должен быть подключён во внешнем источнике данных. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Указывает строку подключения Universal Data Link (UDL), используемую для соединения с внешним источником данных. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Указывает символ, который будет интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию — 0, что означает отсутствие определённого разделителя столбцов.

 **Remarks:** 

RK, я никогда не видел, чтобы это использовалось.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | char | Соответствующее  char  значение. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Указывает расположение внешнего источника данных, который будет подключён к документу для выполнения слияния писем. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Указывает тип внешнего источника данных, который будет подключён в рамках информации о соединении ODSO для этого слияния писем. Значение по умолчанию — [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Эта настройка представляет собой лишь рекомендацию типа источника данных, используемого для этого слияния писем.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одним из констант [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/). |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Устанавливает коллекцию объектов, определяющих, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. Этот объект никогда не является  null .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | Коллекция объектов, определяющих, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Указывает, что хост‑приложение должно рассматривать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена всех столбцов источника. Значение по умолчанию —  false .

 **Remarks:** 

RK, я никогда не видел, чтобы это использовалось.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Устанавливает коллекцию объектов, определяющих включение/исключение отдельных записей при слиянии почты. Этот объект никогда не является  null .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | Коллекция объектов, определяющих включение/исключение отдельных записей при слиянии почты. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Указывает конкретный набор данных, к которому источник должен быть подключён во внешнем источнике данных. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Указывает строку подключения Universal Data Link (UDL), используемую для соединения с внешним источником данных. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

