---
title: XmlDataSource
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступ к данным XML-файла или потока для использования в отчете.
type: docs
weight: 628
url: /ru/java/com.aspose.words/xmldatasource/
---

**Наследование:**
java.lang.Object
```
public class XmlDataSource
```

Предоставляет доступ к данным XML-файла или потока для использования в отчете.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.

 Чтобы получить доступ к данным соответствующего файла или потока при формировании отчета, передайте экземпляр этого класса в качестве источника данных одному из[ReportingEngine](../../com.aspose.words/reportingengine). buildReport перегружается.

 В шаблонных документах, если XML-элемент верхнего уровня содержит только список элементов одного типа,[XmlDataSource](../../com.aspose.words/xmldatasource) экземпляр следует рассматривать так же, как если бы он был[DataTable](../../com.aspose.words.net.system.data/datatable) пример. В противном случае[XmlDataSource](../../com.aspose.words/xmldatasource) экземпляр следует рассматривать так же, как если бы он был[DataRow](../../com.aspose.words.net.system.data/datarow) пример. Дополнительные сведения см. в справочнике по синтаксису шаблона (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Когда определение схемы XML передается конструктору этого класса, типы данных значений простых элементов и атрибутов XML определяются в соответствии со схемой. Таким образом, в шаблонных документах вы можете работать с типизированными значениями, а не только со строками.

Когда определение схемы XML не передается конструктору этого класса, типы данных значений простых элементов и атрибутов XML определяются автоматически на основе их строковых представлений. Таким образом, в шаблонных документах вы также можете работать с типизированными значениями в этом случае. Движок способен автоматически распознавать значения следующих типов:

 *  
 *  
 *  
 *  
 *  

Обратите внимание, что для работы автоматического распознавания типов данных строковые представления значений простых XML-элементов и атрибутов должны быть сформированы с использованием инвариантных настроек культуры.

 Чтобы переопределить поведение загрузки данных XML по умолчанию, инициализируйте и передайте[XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) экземпляр конструктору этого класса.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String-) | Создает новый источник данных с данными из файла XML, используя параметры по умолчанию для загрузки данных XML. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream-) | Инициализирует новый экземпляр этого класса. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String-) | Создает новый источник данных с данными из файла XML, используя файл определения схемы XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream-) | Инициализирует новый экземпляр этого класса. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions-) | Создает новый источник данных с данными из файла XML, используя указанные параметры загрузки данных XML. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-) | Инициализирует новый экземпляр этого класса. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions-) | Создает новый источник данных с данными из файла XML, используя файл определения схемы XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String-}
```
public XmlDataSource(String xmlPath)
```


Создает новый источник данных с данными из файла XML, используя параметры по умолчанию для загрузки данных XML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к файлу XML, который будет использоваться в качестве источника данных. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream-}
```
public XmlDataSource(InputStream xmlStream)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String-}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Создает новый источник данных с данными из файла XML, используя файл определения схемы XML. Параметры по умолчанию используются для загрузки XML-данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к файлу XML, который будет использоваться в качестве источника данных. |
| xmlSchemaPath | java.lang.String | Путь к файлу определения схемы XML, который предоставляет схему для файла XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream-}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Создает новый источник данных с данными из файла XML, используя указанные параметры загрузки данных XML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к файлу XML, который будет использоваться в качестве источника данных. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) | Варианты загрузки XML-данных. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Создает новый источник данных с данными из файла XML, используя файл определения схемы XML. Указанные опции используются для загрузки XML-данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к файлу XML, который будет использоваться в качестве источника данных. |
| xmlSchemaPath | java.lang.String | Путь к файлу определения схемы XML, который предоставляет схему для файла XML. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) | Варианты загрузки XML-данных. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) |  |

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
