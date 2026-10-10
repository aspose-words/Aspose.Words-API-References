---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words для Java"
description: "Указывает всю информацию слияния почты для документа в Java."
type: docs
weight: 445
url: /ru/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Указывает всю информацию о слиянии почты для документа.

Чтобы узнать больше, посетите статью документации [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Вы можете использовать этот объект для указания источника данных слияния почты для документа, и эта информация (вместе с доступными полями данных) будет отображаться в Microsoft Word, когда пользователь откроет документ. Либо вы можете использовать этот объект для запроса настроек слияния почты, которые пользователь указал в Microsoft Word для данного документа.

Обычно вам не требуется создавать объекты этого класса напрямую, поскольку настройки слияния почты документа всегда доступны через свойство [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings).

Чтобы определить, является ли данный документ основным документом слияния почты, проверьте значение свойства [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int).

Чтобы удалить настройки слияния почты и информацию об источнике данных из документа, вы можете использовать метод [clear()](../../com.aspose.words/mailmergesettings/\#clear). Aspose.Words не будет записывать настройки слияния почты в документ, если свойство [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) установлено в значение [MailMergeMainDocumentType.NOT_A_MERGE_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) или свойство [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) установлено в значение [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

Лучший способ изучить, как использовать свойства этого объекта, — создать документ с нужным источником данных вручную в Microsoft Word, затем открыть этот документ с помощью Aspose.Words и изучить свойства объектов [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) и [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). Это хороший подход, если вы хотите узнать, как программно настроить источник данных, например.

Aspose.Words сохраняет информацию о слиянии почты при загрузке, сохранении и конвертации документов между различными форматами, но не использует эту информацию при выполнении собственного слияния почты с помощью объекта [MailMerge](../../com.aspose.words/mailmerge/).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear) | Очищает настройки слияния почты таким образом, что при сохранении документа настройки слияния почты не сохраняются, и документ становится обычным. |
| [deepClone()](#deepClone) | Возвращает глубокую копию этого объекта. |
| [getActiveRecord()](#getActiveRecord) | Указывает одно‑базовый индекс записи из источника данных, который будет отображён в Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName) | Указывает столбец в источнике данных, содержащий адреса электронной почты. |
| [getCheckErrors()](#getCheckErrors) | Указывает тип отчёта об ошибках, который будет выполнен Microsoft Word при выполнении слияния почты. |
| [getConnectString()](#getConnectString) | Указывает строку подключения, используемую для соединения с внешним источником данных. |
| [getDataSource()](#getDataSource) | Указывает путь к источнику данных слияния почты. |
| [getDataType()](#getDataType) | Указывает тип источника данных слияния почты и метод доступа к данным. |
| [getDestination()](#getDestination) | Указывает, как Microsoft Word будет выводить результаты слияния почты. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединённых документах, полученных в результате слияния почты. |
| [getHeaderSource()](#getHeaderSource) | Указывает путь к источнику заголовка слияния почты. |
| [getLinkToQuery()](#getLinkToQuery) | Не уверен в этом. |
| [getMailAsAttachment()](#getMailAsAttachment) | Указывает, что документы, созданные во время операции слияния почты, должны отправляться по электронной почте в виде вложения, а не в теле самого письма. |
| [getMailSubject()](#getMailSubject) | Указывает текст, который должен отображаться в строке темы электронных писем или факсов, созданных во время слияния почты. |
| [getMainDocumentType()](#getMainDocumentType) | Указывает основной тип документа слияния почты. |
| [getOdso()](#getOdso) | Получает объект, который задаёт параметры Office Data Source Object (ODSO). |
| [getQuery()](#getQuery) | Содержит строку Structured Query Language, которая должна быть выполнена против указанного внешнего источника данных, чтобы вернуть набор записей, которые будут импортированы в документ при выполнении операции слияния почты. |
| [getViewMergedData()](#getViewMergedData) | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных там, где вставлены поля слияния (например, |
| [setActiveRecord(int value)](#setActiveRecord-int) | Указывает одно‑базовый индекс записи из источника данных, который будет отображён в Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | Указывает столбец в источнике данных, содержащий адреса электронной почты. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Указывает тип отчёта об ошибках, который будет выполнен Microsoft Word при выполнении слияния почты. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Указывает строку подключения, используемую для соединения с внешним источником данных. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Указывает путь к источнику данных слияния почты. |
| [setDataType(int value)](#setDataType-int) | Указывает тип источника данных слияния почты и метод доступа к данным. |
| [setDestination(int value)](#setDestination-int) | Указывает, как Microsoft Word будет выводить результаты слияния почты. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединённых документах, полученных в результате слияния почты. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Указывает путь к источнику заголовка слияния почты. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | Не уверен в этом. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Указывает, что документы, созданные во время операции слияния почты, должны отправляться по электронной почте в виде вложения, а не в теле самого письма. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Указывает текст, который должен отображаться в строке темы электронных писем или факсов, созданных во время слияния почты. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Указывает основной тип документа слияния почты. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Устанавливает объект, который задаёт параметры Office Data Source Object (ODSO). |
| [setQuery(String value)](#setQuery-java.lang.String) | Содержит строку Structured Query Language, которая должна быть выполнена против указанного внешнего источника данных, чтобы вернуть набор записей, которые будут импортированы в документ при выполнении операции слияния почты. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных там, где вставлены поля слияния (например, |
### clear() {#clear}
```
public void clear()
```


Очищает настройки слияния почты таким образом, что при сохранении документа настройки слияния почты не сохраняются, и документ становится обычным.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Возвращает глубокую копию этого объекта.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Указывает индекс записи из источника данных, начинающийся с единицы, который должен отображаться в Microsoft Word. Значение по умолчанию — 1.

**Returns:**
int — соответствующее значение  int .
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Указывает столбец в источнике данных, содержащий адреса электронной почты. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Указывает тип отчётов об ошибках, которые будет выполнять Microsoft Word при выполнении слияния почты. Значение по умолчанию — [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int — соответствующее значение int. Возвращаемое значение является одной из констант [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/).
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Указывает строку подключения, используемую для соединения с внешним источником данных. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Указывает путь к источнику данных слияния почты. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getDataType() {#getDataType}
```
public int getDataType()
```


Указывает тип источника данных слияния почты и метод доступа к данным. Значение по умолчанию — [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int — соответствующее значение int. Возвращаемое значение является одной из констант [MailMergeDataType](../../com.aspose.words/mailmergedatatype/).
### getDestination() {#getDestination}
```
public int getDestination()
```


Указывает, как Microsoft Word будет выводить результаты слияния почты. Значение по умолчанию — [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int — соответствующее значение int. Возвращаемое значение является одной из констант [MailMergeDestination](../../com.aspose.words/mailmergedestination/).
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединённых документах, полученных в результате слияния почты. Значение по умолчанию — false.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Указывает путь к источнику заголовка слияния почты. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


Не уверен в этом. Ссылка Microsoft Word Automation Reference подразумевает, что это указывает на то, что запрос выполняется каждый раз при открытии документа в Microsoft Word. Но спецификация OOXML подразумевает, что это указывает на то, что запрос содержит ссылку на внешний файл запроса, который содержит фактический запрос. Значение по умолчанию — false.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Указывает, что документы, созданные во время операции слияния почты, должны отправляться по электронной почте в виде вложения, а не в теле самого письма. Значение по умолчанию — false.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Указывает текст, который будет отображаться в строке темы электронных писем или факсов, создаваемых при слиянии почты. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Указывает тип основного документа слияния почты. Значение по умолчанию — [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Основной документ — это документ, содержащий информацию, одинаковую для каждой версии объединённого документа.

**Returns:**
int — соответствующее значение  int . Возвращаемое значение является одной из констант [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/).
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Получает объект, который задаёт параметры Office Data Source Object (ODSO).

 **Remarks:** 

Этот объект никогда не  null .

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Содержит строку Structured Query Language, которая будет выполнена против указанного внешнего источника данных для возврата набора записей, которые будут импортированы в документ при выполнении операции слияния почты. Значение по умолчанию — пустая строка.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных там, где вставлены поля слияния (например, предварительный просмотр объединённых данных). Значение по умолчанию —  false .

**Returns:**
boolean - Соответствующее  boolean  значение.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Указывает индекс записи из источника данных, начинающийся с единицы, который должен отображаться в Microsoft Word. Значение по умолчанию — 1.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Указывает столбец в источнике данных, содержащий адреса электронной почты. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Указывает тип отчётов об ошибках, которые будет выполнять Microsoft Word при выполнении слияния почты. Значение по умолчанию — [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение  int . Значение должно быть одной из констант [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/). |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Указывает строку подключения, используемую для соединения с внешним источником данных. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Указывает путь к источнику данных слияния почты. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Указывает тип источника данных слияния почты и метод доступа к данным. Значение по умолчанию — [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение  int . Значение должно быть одной из констант [MailMergeDataType](../../com.aspose.words/mailmergedatatype/). |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Указывает, как Microsoft Word будет выводить результаты слияния почты. Значение по умолчанию — [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение  int . Значение должно быть одной из констант [MailMergeDestination](../../com.aspose.words/mailmergedestination/). |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединённых документах, полученных в результате слияния почты. Значение по умолчанию — false.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Указывает путь к источнику заголовка слияния почты. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


Не уверен в этом. Ссылка Microsoft Word Automation Reference подразумевает, что это указывает на то, что запрос выполняется каждый раз при открытии документа в Microsoft Word. Но спецификация OOXML подразумевает, что это указывает на то, что запрос содержит ссылку на внешний файл запроса, который содержит фактический запрос. Значение по умолчанию — false.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Указывает, что документы, созданные во время операции слияния почты, должны отправляться по электронной почте в виде вложения, а не в теле самого письма. Значение по умолчанию — false.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Указывает текст, который будет отображаться в строке темы электронных писем или факсов, создаваемых при слиянии почты. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Указывает тип основного документа слияния почты. Значение по умолчанию — [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Основной документ — это документ, содержащий информацию, одинаковую для каждой версии объединённого документа.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение  int . Значение должно быть одной из констант [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/). |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Устанавливает объект, который задаёт параметры Office Data Source Object (ODSO).

 **Remarks:** 

Этот объект никогда не  null .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | Объект, который задает параметры Office Data Source Object (ODSO). |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Содержит строку Structured Query Language, которая будет выполнена против указанного внешнего источника данных для возврата набора записей, которые будут импортированы в документ при выполнении операции слияния почты. Значение по умолчанию — пустая строка.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных там, где вставлены поля слияния (например, предварительный просмотр объединённых данных). Значение по умолчанию —  false .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

