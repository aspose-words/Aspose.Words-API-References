---
title: Odso
second_title: Справочник по API Aspose.Words для Java
description: Указывает параметры ODSO объекта источника данных Office для источника данных слияния.
type: docs
weight: 411
url: /ru/java/com.aspose.words/odso/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Указывает параметры объекта источника данных Office (ODSO) для источника данных слияния.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

ODSO кажется «новым» способом, который предпочитают использовать более новые версии Microsoft Word при указании определенных типов источников данных для документа слияния. ODSO, вероятно, впервые появился в Microsoft Word 2000.

Использование ODSO плохо документировано, и лучший способ узнать, как использовать свойства этого объекта, — создать документ с нужным источником данных вручную в Microsoft Word, а затем открыть этот документ с помощью Aspose.Words и изучить свойства объекта.[Document.getMailMergeSettings()](../../com.aspose.words/document\#getMailMergeSettings--) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document\#setMailMergeSettings-com.aspose.words.MailMergeSettings-) а также[MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings\#getOdso--) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings\#setOdso-com.aspose.words.Odso-)объекты. Это хороший подход, если вы хотите научиться, например, программно настраивать источник данных.

 Обычно вам не нужно создавать объекты этого класса напрямую, потому что настройки ODSO всегда доступны через[MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings\#getOdso--) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings\#setOdso-com.aspose.words.Odso-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [deepClone()](#deepClone--) | Возвращает глубокий клон этого объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColumnDelimiter()](#getColumnDelimiter--) | Задает символ, который следует интерпретировать как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. |
| [getDataSource()](#getDataSource--) | Указывает расположение внешнего источника данных, который необходимо подключить к документу для выполнения слияния. |
| [getDataSourceType()](#getDataSourceType--) | Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть сведений о соединении ODSO для этого слияния. |
| [getFieldMapDatas()](#getFieldMapDatas--) | Получает коллекцию объектов, указывающих, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames--) | Указывает, что хост-приложение должно обрабатывать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена каждого столбца в источнике данных. |
| [getRecipientDatas()](#getRecipientDatas--) | Получает коллекцию объектов, указывающих включение или исключение отдельных записей при слиянии. |
| [getTableName()](#getTableName--) | Указывает конкретный набор данных, к которому должен быть подключен источник во внешнем источнике данных. |
| [getUdlConnectString()](#getUdlConnectString--) | Задает строку подключения к универсальному каналу передачи данных (UDL), используемую для подключения к внешнему источнику данных. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char-) | Задает символ, который следует интерпретировать как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. |
| [setDataSource(String value)](#setDataSource-java.lang.String-) | Указывает расположение внешнего источника данных, который необходимо подключить к документу для выполнения слияния. |
| [setDataSourceType(int value)](#setDataSourceType-int-) | Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть сведений о соединении ODSO для этого слияния. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection-) | Задает набор объектов, указывающих, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean-) | Указывает, что хост-приложение должно обрабатывать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена каждого столбца в источнике данных. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection-) | Задает набор объектов, определяющих включение/исключение отдельных записей при слиянии. |
| [setTableName(String value)](#setTableName-java.lang.String-) | Указывает конкретный набор данных, к которому должен быть подключен источник во внешнем источнике данных. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String-) | Задает строку подключения к универсальному каналу передачи данных (UDL), используемую для подключения к внешнему источнику данных. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public Odso deepClone()
```


Возвращает глубокий клон этого объекта.

**Возвращает:**
[Odso](../../com.aspose.words/odso)
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
### getColumnDelimiter() {#getColumnDelimiter--}
```
public char getColumnDelimiter()
```


Задает символ, который следует интерпретировать как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию равно 0, что означает, что разделитель столбцов не определен.

РК Я никогда не видел это в использовании.

**Возвращает:**
char - соответствующее значение char.
### getDataSource() {#getDataSource--}
```
public String getDataSource()
```


Указывает расположение внешнего источника данных, который необходимо подключить к документу для выполнения слияния. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getDataSourceType() {#getDataSourceType--}
```
public int getDataSourceType()
```


 Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть сведений о соединении ODSO для этого слияния. Значение по умолчанию[OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype\#DEFAULT).

Этот параметр является всего лишь предложением типа источника данных, который используется для этого слияния.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype) константы.
### getFieldMapDatas() {#getFieldMapDatas--}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Получает коллекцию объектов, указывающих, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. Этот объект никогда не бывает нулевым.

**Возвращает:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection) - Набор объектов, указывающих, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames--}
```
public boolean getFirstRowContainsColumnNames()
```


Указывает, что хост-приложение должно обрабатывать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена каждого столбца в источнике данных. Значение по умолчанию неверно .

РК Я никогда не видел это в использовании.

**Возвращает:**
boolean - соответствующее логическое значение.
### getRecipientDatas() {#getRecipientDatas--}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Получает коллекцию объектов, указывающих включение или исключение отдельных записей при слиянии. Этот объект никогда не бывает нулевым.

**Возвращает:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection) - Набор объектов, определяющих включение/исключение отдельных записей в слиянии.
### getTableName() {#getTableName--}
```
public String getTableName()
```


Указывает конкретный набор данных, к которому должен быть подключен источник во внешнем источнике данных. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getUdlConnectString() {#getUdlConnectString--}
```
public String getUdlConnectString()
```


Задает строку подключения к универсальному каналу передачи данных (UDL), используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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




### setColumnDelimiter(char value) {#setColumnDelimiter-char-}
```
public void setColumnDelimiter(char value)
```


Задает символ, который следует интерпретировать как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию равно 0, что означает, что разделитель столбцов не определен.

РК Я никогда не видел это в использовании.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | char | Соответствующее значение char. |

### setDataSource(String value) {#setDataSource-java.lang.String-}
```
public void setDataSource(String value)
```


Указывает расположение внешнего источника данных, который необходимо подключить к документу для выполнения слияния. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDataSourceType(int value) {#setDataSourceType-int-}
```
public void setDataSourceType(int value)
```


 Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть сведений о соединении ODSO для этого слияния. Значение по умолчанию[OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype\#DEFAULT).

Этот параметр является всего лишь предложением типа источника данных, который используется для этого слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype) константы. |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection-}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Задает набор объектов, указывающих, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. Этот объект никогда не бывает нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection) | Коллекция объектов, указывающая, как столбцы из внешнего источника данных сопоставляются с предопределенными именами полей слияния в документе. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean-}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Указывает, что хост-приложение должно обрабатывать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена каждого столбца в источнике данных. Значение по умолчанию неверно .

РК Я никогда не видел это в использовании.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection-}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Задает набор объектов, определяющих включение/исключение отдельных записей при слиянии. Этот объект никогда не бывает нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection) | Набор объектов, определяющих включение/исключение отдельных записей в слиянии. |

### setTableName(String value) {#setTableName-java.lang.String-}
```
public void setTableName(String value)
```


Указывает конкретный набор данных, к которому должен быть подключен источник во внешнем источнике данных. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String-}
```
public void setUdlConnectString(String value)
```


Задает строку подключения к универсальному каналу передачи данных (UDL), используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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
