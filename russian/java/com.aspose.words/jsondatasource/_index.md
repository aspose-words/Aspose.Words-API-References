---
title: JsonDataSource
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступ к данным файла или потока JSON для использования в отчете.
type: docs
weight: 354
url: /ru/java/com.aspose.words/jsondatasource/
---

**Наследование:**
java.lang.Object
```
public class JsonDataSource
```

Предоставляет доступ к данным файла или потока JSON для использования в отчете.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.

 Чтобы получить доступ к данным соответствующего файла или потока при формировании отчета, передайте экземпляр этого класса в качестве источника данных одному из[ReportingEngine](../../com.aspose.words/reportingengine). buildReport перегружается.

 В шаблонных документах, если элемент JSON верхнего уровня является массивом,[JsonDataSource](../../com.aspose.words/jsondatasource) экземпляр следует рассматривать так же, как если бы он был[DataTable](../../com.aspose.words.net.system.data/datatable) пример. Если элемент JSON верхнего уровня является объектом,[JsonDataSource](../../com.aspose.words/jsondatasource) экземпляр следует рассматривать так же, как если бы он был[DataRow](../../com.aspose.words.net.system.data/datarow) пример. Дополнительные сведения см. в справочнике по синтаксису шаблона (https://docs.aspose.com/display/wordsjava/Template+Syntax).

В шаблонных документах можно работать с типизированными значениями элементов JSON. Для удобства движок заменяет набор простых типов JSON на следующий:

 *  
 *  
 *  
 *  
 *  

Механизм автоматически распознает значения дополнительных типов по их представлениям JSON.

Чтобы переопределить поведение загрузки данных JSON по умолчанию, инициализируйте и передайте[JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions) экземпляр конструктору этого класса.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String-) | Создает новый источник данных с данными из файла JSON, используя параметры по умолчанию для анализа данных JSON. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream-) | Инициализирует новый экземпляр этого класса. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions-) | Создает новый источник данных с данными из файла JSON, используя указанные параметры анализа данных JSON. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions-) | Инициализирует новый экземпляр этого класса. |
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
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String-}
```
public JsonDataSource(String jsonPath)
```


Создает новый источник данных с данными из файла JSON, используя параметры по умолчанию для анализа данных JSON.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonPath | java.lang.String | Путь к файлу JSON, который будет использоваться в качестве источника данных. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream-}
```
public JsonDataSource(InputStream jsonStream)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions-}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Создает новый источник данных с данными из файла JSON, используя указанные параметры анализа данных JSON.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonPath | java.lang.String | Путь к файлу JSON, который будет использоваться в качестве источника данных. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions) | Параметры для анализа данных JSON. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions-}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions) |  |

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
