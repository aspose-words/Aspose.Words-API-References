---
title: CsvDataSource
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступ к данным CSV-файла или потока для использования в отчете.
type: docs
weight: 99
url: /ru/java/com.aspose.words/csvdatasource/
---

**Наследование:**
java.lang.Object
```
public class CsvDataSource
```

Предоставляет доступ к данным CSV-файла или потока для использования в отчете.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.

 Чтобы получить доступ к данным соответствующего файла или потока при формировании отчета, передайте экземпляр этого класса в качестве источника данных одному из[ReportingEngine](../../com.aspose.words/reportingengine). buildReport перегружается.

 В шаблонных документах[CsvDataSource](../../com.aspose.words/csvdatasource) экземпляр следует рассматривать так же, как если бы он был[DataTable](../../com.aspose.words.net.system.data/datatable) пример. Дополнительные сведения см. в справочнике по синтаксису шаблона (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Типы данных значений, разделенных запятыми, определяются автоматически при их строковом представлении. Таким образом, в шаблонных документах вы можете работать с типизированными значениями, а не только со строками. Движок способен автоматически распознавать значения следующих типов:

 *  
 *  
 *  
 *  
 *  

Обратите внимание, что для работы автоматического распознавания типов данных строковые представления значений, разделенных запятыми, должны быть сформированы с использованием инвариантных настроек языка и региональных параметров.

 Чтобы переопределить поведение загрузки данных CSV по умолчанию, инициализируйте и передайте[CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions) экземпляр конструктору этого класса.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String-) | Создает новый источник данных с данными из файла CSV, используя параметры по умолчанию для анализа данных CSV. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions-) | Создает новый источник данных с данными из файла CSV, используя указанные параметры анализа данных CSV. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream-) | Инициализирует новый экземпляр этого класса. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions-) | Инициализирует новый экземпляр этого класса. |
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
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String-}
```
public CsvDataSource(String csvPath)
```


Создает новый источник данных с данными из файла CSV, используя параметры по умолчанию для анализа данных CSV.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvPath | java.lang.String | Путь к CSV-файлу, который будет использоваться в качестве источника данных. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions-}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Создает новый источник данных с данными из файла CSV, используя указанные параметры анализа данных CSV.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvPath | java.lang.String | Путь к CSV-файлу, который будет использоваться в качестве источника данных. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions) | Параметры для анализа данных CSV. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream-}
```
public CsvDataSource(InputStream csvStream)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions-}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions) |  |

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
