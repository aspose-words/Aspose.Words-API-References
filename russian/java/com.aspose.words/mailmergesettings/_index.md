---
title: MailMergeSettings
second_title: Справочник по API Aspose.Words для Java
description: Указывает всю информацию о слиянии для документа.
type: docs
weight: 386
url: /ru/java/com.aspose.words/mailmergesettings/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Указывает всю информацию о слиянии для документа.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

Вы можете использовать этот объект, чтобы указать источник данных слияния для документа, и эта информация (вместе с доступными полями данных) появится в Microsoft Word, когда пользователь откроет этот документ. Или вы можете использовать этот объект для запроса настроек слияния, которые пользователь указал в Microsoft Word для этого документа.

 Обычно вам не нужно создавать объекты этого класса напрямую, потому что настройки слияния документов всегда доступны через[Document.getMailMergeSettings()](../../com.aspose.words/document\#getMailMergeSettings--) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document\#setMailMergeSettings-com.aspose.words.MailMergeSettings-) имущество.

 Чтобы определить, является ли этот документ основным документом слияния, проверьте значение[getMainDocumentType()](../../com.aspose.words/mailmergesettings\#getMainDocumentType--) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings\#setMainDocumentType-int-) имущество.

 Чтобы удалить настройки слияния и информацию об источнике данных из документа, вы можете использовать[clear()](../../com.aspose.words/mailmergesettings\#clear--) метод. Aspose.Words не будет записывать настройки слияния в документ, если[getMainDocumentType()](../../com.aspose.words/mailmergesettings\#getMainDocumentType--) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings\#setMainDocumentType-int-) свойство установлено на[MailMergeMainDocumentType.NOT\_A\_MERGE\_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype\#NOT-A-MERGE-DOCUMENT) или[getDataType()](../../com.aspose.words/mailmergesettings\#getDataType--) / [setDataType(int)](../../com.aspose.words/mailmergesettings\#setDataType-int-) свойство установлено на[MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype\#NONE).

 Лучший способ научиться использовать свойства этого объекта — создать документ с нужным источником данных вручную в Microsoft Word, а затем открыть этот документ с помощью Aspose.Words и изучить свойства объекта.[Document.getMailMergeSettings()](../../com.aspose.words/document\#getMailMergeSettings--) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document\#setMailMergeSettings-com.aspose.words.MailMergeSettings-) а также[getOdso()](../../com.aspose.words/mailmergesettings\#getOdso--) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings\#setOdso-com.aspose.words.Odso-)объекты. Это хороший подход, если вы хотите научиться, например, программно настраивать источник данных.

 Aspose.Words сохраняет информацию о слиянии при загрузке, сохранении и преобразовании документов между различными форматами, но не использует эту информацию при выполнении собственного слияния с помощью[MailMerge](../../com.aspose.words/mailmerge) объект.
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Очищает настройки слияния таким образом, что при сохранении документа никакие настройки слияния не сохраняются, и он становится обычным документом. |
| [deepClone()](#deepClone--) | Возвращает глубокий клон этого объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getActiveRecord()](#getActiveRecord--) | Указывает индекс записи из источника данных, который должен отображаться в Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName--) | Указывает столбец в источнике данных, который содержит адреса электронной почты. |
| [getCheckErrors()](#getCheckErrors--) | Указывает тип отчетов об ошибках, которые должны создаваться Microsoft Word при выполнении слияния. |
| [getClass()](#getClass--) |  |
| [getConnectString()](#getConnectString--) | Указывает строку подключения, используемую для подключения к внешнему источнику данных. |
| [getDataSource()](#getDataSource--) | Указывает путь к источнику данных для слияния. |
| [getDataType()](#getDataType--) | Указывает тип источника данных для слияния и метод доступа к данным. |
| [getDestination()](#getDestination--) | Указывает, как Microsoft Word будет выводить результаты слияния. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines--) | Указывает, как приложение, выполняющее слияние, должно обрабатывать пустые строки в объединенных документах, полученных в результате слияния. |
| [getHeaderSource()](#getHeaderSource--) | Указывает путь к источнику заголовка слияния. |
| [getLinkToQuery()](#getLinkToQuery--) | Не уверен насчет этого. |
| [getMailAsAttachment()](#getMailAsAttachment--) | Указывает, что документы, созданные во время операции слияния, следует отправлять по электронной почте в виде вложений, а не в виде тела фактического сообщения электронной почты. |
| [getMailSubject()](#getMailSubject--) | Определяет текст, который должен отображаться в строке темы сообщений электронной почты или факсов, созданных во время слияния. |
| [getMainDocumentType()](#getMainDocumentType--) | Указывает тип основного документа для слияния. |
| [getOdso()](#getOdso--) | Получает объект, указывающий параметры объекта источника данных Office (ODSO). |
| [getQuery()](#getQuery--) | Содержит строку языка структурированных запросов, которая должна выполняться для указанного внешнего источника данных, чтобы вернуть набор записей, которые должны быть импортированы в документ при выполнении операции слияния. |
| [getViewMergedData()](#getViewMergedData--) | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных, в который были вставлены поля слияния (например, |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setActiveRecord(int value)](#setActiveRecord-int-) | Указывает индекс записи из источника данных, который должен отображаться в Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String-) | Указывает столбец в источнике данных, который содержит адреса электронной почты. |
| [setCheckErrors(int value)](#setCheckErrors-int-) | Указывает тип отчетов об ошибках, которые должны создаваться Microsoft Word при выполнении слияния. |
| [setConnectString(String value)](#setConnectString-java.lang.String-) | Указывает строку подключения, используемую для подключения к внешнему источнику данных. |
| [setDataSource(String value)](#setDataSource-java.lang.String-) | Указывает путь к источнику данных для слияния. |
| [setDataType(int value)](#setDataType-int-) | Указывает тип источника данных для слияния и метод доступа к данным. |
| [setDestination(int value)](#setDestination-int-) | Указывает, как Microsoft Word будет выводить результаты слияния. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean-) | Указывает, как приложение, выполняющее слияние, должно обрабатывать пустые строки в объединенных документах, полученных в результате слияния. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String-) | Указывает путь к источнику заголовка слияния. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean-) | Не уверен насчет этого. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean-) | Указывает, что документы, созданные во время операции слияния, следует отправлять по электронной почте в виде вложений, а не в виде тела фактического сообщения электронной почты. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String-) | Определяет текст, который должен отображаться в строке темы сообщений электронной почты или факсов, созданных во время слияния. |
| [setMainDocumentType(int value)](#setMainDocumentType-int-) | Указывает тип основного документа для слияния. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso-) | Задает объект, указывающий параметры объекта источника данных Office (ODSO). |
| [setQuery(String value)](#setQuery-java.lang.String-) | Содержит строку языка структурированных запросов, которая должна выполняться для указанного внешнего источника данных, чтобы вернуть набор записей, которые должны быть импортированы в документ при выполнении операции слияния. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean-) | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных, в который были вставлены поля слияния (например, |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


Очищает настройки слияния таким образом, что при сохранении документа никакие настройки слияния не сохраняются, и он становится обычным документом.

### deepClone() {#deepClone--}
```
public MailMergeSettings deepClone()
```


Возвращает глубокий клон этого объекта.

**Возвращает:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings)
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
### getActiveRecord() {#getActiveRecord--}
```
public int getActiveRecord()
```


Указывает индекс записи из источника данных, который должен отображаться в Microsoft Word. Значение по умолчанию — 1.

**Возвращает:**
int - соответствующее значение int.
### getAddressFieldName() {#getAddressFieldName--}
```
public String getAddressFieldName()
```


Указывает столбец в источнике данных, который содержит адреса электронной почты. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getCheckErrors() {#getCheckErrors--}
```
public int getCheckErrors()
```


 Указывает тип отчетов об ошибках, которые должны создаваться Microsoft Word при выполнении слияния. Значение по умолчанию[MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors\#DEFAULT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors) константы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getConnectString() {#getConnectString--}
```
public String getConnectString()
```


Указывает строку подключения, используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getDataSource() {#getDataSource--}
```
public String getDataSource()
```


Указывает путь к источнику данных для слияния. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getDataType() {#getDataType--}
```
public int getDataType()
```


 Указывает тип источника данных для слияния и метод доступа к данным. Значение по умолчанию[MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype\#DEFAULT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MailMergeDataType](../../com.aspose.words/mailmergedatatype) константы.
### getDestination() {#getDestination--}
```
public int getDestination()
```


Указывает, как Microsoft Word будет выводить результаты слияния. Значение по умолчанию[MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination\#DEFAULT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MailMergeDestination](../../com.aspose.words/mailmergedestination) константы.
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines--}
```
public boolean getDoNotSupressBlankLines()
```


Указывает, как приложение, выполняющее слияние, должно обрабатывать пустые строки в объединенных документах, полученных в результате слияния. Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
### getHeaderSource() {#getHeaderSource--}
```
public String getHeaderSource()
```


Указывает путь к источнику заголовка слияния. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getLinkToQuery() {#getLinkToQuery--}
```
public boolean getLinkToQuery()
```


Не уверен насчет этого. Справочник по автоматизации Microsoft Word предполагает, что это указывает, что запрос выполняется каждый раз, когда документ открывается в Microsoft Word. Но спецификация OOXML предполагает, что это указывает на то, что запрос содержит ссылку на внешний файл запроса, который содержит фактический запрос. Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
### getMailAsAttachment() {#getMailAsAttachment--}
```
public boolean getMailAsAttachment()
```


Указывает, что документы, созданные во время операции слияния, следует отправлять по электронной почте в виде вложений, а не в виде тела фактического сообщения электронной почты. Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
### getMailSubject() {#getMailSubject--}
```
public String getMailSubject()
```


Определяет текст, который должен отображаться в строке темы сообщений электронной почты или факсов, созданных во время слияния. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getMainDocumentType() {#getMainDocumentType--}
```
public int getMainDocumentType()
```


 Указывает тип основного документа для слияния. Значение по умолчанию[MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype\#DEFAULT).

Основной документ — это документ, содержащий информацию, одинаковую для каждой версии объединенного документа.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype) константы.
### getOdso() {#getOdso--}
```
public Odso getOdso()
```


Получает объект, указывающий параметры объекта источника данных Office (ODSO).

Этот объект никогда не бывает нулевым.

**Возвращает:**
[Odso](../../com.aspose.words/odso) - Объект, указывающий параметры объекта источника данных Office (ODSO).
### getQuery() {#getQuery--}
```
public String getQuery()
```


Содержит строку языка структурированных запросов, которая должна выполняться для указанного внешнего источника данных, чтобы вернуть набор записей, которые должны быть импортированы в документ при выполнении операции слияния. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getViewMergedData() {#getViewMergedData--}
```
public boolean getViewMergedData()
```


Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных, в который были вставлены поля слияния (например, предварительный просмотр объединенных данных). Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
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




### setActiveRecord(int value) {#setActiveRecord-int-}
```
public void setActiveRecord(int value)
```


Указывает индекс записи из источника данных, который должен отображаться в Microsoft Word. Значение по умолчанию — 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String-}
```
public void setAddressFieldName(String value)
```


Указывает столбец в источнике данных, который содержит адреса электронной почты. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setCheckErrors(int value) {#setCheckErrors-int-}
```
public void setCheckErrors(int value)
```


 Указывает тип отчетов об ошибках, которые должны создаваться Microsoft Word при выполнении слияния. Значение по умолчанию[MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors\#DEFAULT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors) константы. |

### setConnectString(String value) {#setConnectString-java.lang.String-}
```
public void setConnectString(String value)
```


Указывает строку подключения, используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDataSource(String value) {#setDataSource-java.lang.String-}
```
public void setDataSource(String value)
```


Указывает путь к источнику данных для слияния. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDataType(int value) {#setDataType-int-}
```
public void setDataType(int value)
```


 Указывает тип источника данных для слияния и метод доступа к данным. Значение по умолчанию[MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype\#DEFAULT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MailMergeDataType](../../com.aspose.words/mailmergedatatype) константы. |

### setDestination(int value) {#setDestination-int-}
```
public void setDestination(int value)
```


Указывает, как Microsoft Word будет выводить результаты слияния. Значение по умолчанию[MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination\#DEFAULT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MailMergeDestination](../../com.aspose.words/mailmergedestination) константы. |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean-}
```
public void setDoNotSupressBlankLines(boolean value)
```


Указывает, как приложение, выполняющее слияние, должно обрабатывать пустые строки в объединенных документах, полученных в результате слияния. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String-}
```
public void setHeaderSource(String value)
```


Указывает путь к источнику заголовка слияния. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean-}
```
public void setLinkToQuery(boolean value)
```


Не уверен насчет этого. Справочник по автоматизации Microsoft Word предполагает, что это указывает, что запрос выполняется каждый раз, когда документ открывается в Microsoft Word. Но спецификация OOXML предполагает, что это указывает на то, что запрос содержит ссылку на внешний файл запроса, который содержит фактический запрос. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean-}
```
public void setMailAsAttachment(boolean value)
```


Указывает, что документы, созданные во время операции слияния, следует отправлять по электронной почте в виде вложений, а не в виде тела фактического сообщения электронной почты. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setMailSubject(String value) {#setMailSubject-java.lang.String-}
```
public void setMailSubject(String value)
```


Определяет текст, который должен отображаться в строке темы сообщений электронной почты или факсов, созданных во время слияния. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setMainDocumentType(int value) {#setMainDocumentType-int-}
```
public void setMainDocumentType(int value)
```


 Указывает тип основного документа для слияния. Значение по умолчанию[MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype\#DEFAULT).

Основной документ — это документ, содержащий информацию, одинаковую для каждой версии объединенного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype) константы. |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso-}
```
public void setOdso(Odso value)
```


Задает объект, указывающий параметры объекта источника данных Office (ODSO).

Этот объект никогда не бывает нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso) | Объект, указывающий параметры объекта источника данных Office (ODSO). |

### setQuery(String value) {#setQuery-java.lang.String-}
```
public void setQuery(String value)
```


Содержит строку языка структурированных запросов, которая должна выполняться для указанного внешнего источника данных, чтобы вернуть набор записей, которые должны быть импортированы в документ при выполнении операции слияния. Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean-}
```
public void setViewMergedData(boolean value)
```


Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных, в который были вставлены поля слияния (например, предварительный просмотр объединенных данных). Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
