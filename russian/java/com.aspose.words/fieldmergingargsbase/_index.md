---
title: FieldMergingArgsBase
second_title: Справочник по API Aspose.Words для Java
description: Базовый класс для и .
type: docs
weight: 219
url: /ru/java/com.aspose.words/fieldmergingargsbase/
---

**Наследование:**
java.lang.Object
```
public abstract class FieldMergingArgsBase
```

 Базовый класс для[FieldMergingArgs](../../com.aspose.words/fieldmergingargs) а также[ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs).

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FieldMergingArgsBase()](#FieldMergingArgsBase--) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) |  Возвращает[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) объект, для которого выполняется слияние. |
| [getDocumentFieldName()](#getDocumentFieldName--) | Получает имя поля слияния, указанное в документе. |
| [getField()](#getField--) | Получает объект, представляющий текущее поле слияния. |
| [getFieldName()](#getFieldName--) | Получает имя поля слияния в источнике данных. |
| [getFieldValue()](#getFieldValue--) | Получает значение поля из источника данных. |
| [getRecordIndex()](#getRecordIndex--) | Получает отсчитываемый от нуля индекс объединяемой записи. |
| [getTableName()](#getTableName--) | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object-) | Задает значение поля из источника данных. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FieldMergingArgsBase() {#FieldMergingArgsBase--}
```
public FieldMergingArgsBase()
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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


 Возвращает[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) объект, для которого выполняется слияние.

**Возвращает:**
[Document](../../com.aspose.words/document) -[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) объект, для которого выполняется слияние.
### getDocumentFieldName() {#getDocumentFieldName--}
```
public String getDocumentFieldName()
```


Получает имя поля слияния, указанное в документе.

Если у вас есть сопоставление имени поля документа с другим именем поля источника данных, то это исходное имя поля, указанное в документе.

 Если вы указали в документе префикс имени поля, например «Image:MyFieldName», то**DocumentFieldName** возвращает имя поля без префикса, то есть "MyFieldName".

**Возвращает:**
java.lang.String — имя поля слияния, указанное в документе.
### getField() {#getField--}
```
public FieldMergeField getField()
```


Получает объект, представляющий текущее поле слияния.

**Возвращает:**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - Объект, представляющий текущее поле слияния.
### getFieldName() {#getFieldName--}
```
public String getFieldName()
```


Получает имя поля слияния в источнике данных.

Если у вас есть сопоставление имени поля документа с другим именем поля источника данных, то это имя сопоставленного поля.

 Если вы указали в документе префикс имени поля, например «Image:MyFieldName», то**FieldName** возвращает имя поля без префикса, то есть "MyFieldName".

**Возвращает:**
java.lang.String — имя поля слияния в источнике данных.
### getFieldValue() {#getFieldValue--}
```
public Object getFieldValue()
```


Получает значение поля из источника данных. Это свойство содержит значение, которое только что было выбрано из вашего источника данных для этого поля механизмом слияния. Вы также можете заменить значение, установив свойство.

**Возвращает:**
java.lang.Object — значение поля из источника данных.
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


Получает отсчитываемый от нуля индекс объединяемой записи.

**Возвращает:**
int — индекс объединяемой записи с отсчетом от нуля.
### getTableName() {#getTableName--}
```
public String getTableName()
```


Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно.

**Возвращает:**
java.lang.String — имя таблицы данных для текущей операции слияния или пустая строка, если имя недоступно.
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




### setFieldValue(Object value) {#setFieldValue-java.lang.Object-}
```
public void setFieldValue(Object value)
```


Задает значение поля из источника данных. Это свойство содержит значение, которое только что было выбрано из вашего источника данных для этого поля механизмом слияния. Вы также можете заменить значение, установив свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object | Значение поля из источника данных. |

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
