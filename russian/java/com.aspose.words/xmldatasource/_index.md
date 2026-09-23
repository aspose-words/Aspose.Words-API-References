---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words для Java"
description: "Обеспечивает доступ к данным XML‑файла или потока, которые будут использоваться в отчете в Java."
type: docs
weight: 746
url: /ru/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Обеспечивает доступ к данным XML‑файла или потока, которые будут использоваться в отчёте.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Чтобы получить доступ к данным соответствующего файла или потока при генерации отчёта, передайте экземпляр этого класса в качестве источника данных в один из методов [ReportingEngine](../../com.aspose.words/reportingengine/). перегрузки buildReport.

В шаблонных документах, если элемент верхнего уровня XML содержит только список элементов одного типа, экземпляр [XmlDataSource](../../com.aspose.words/xmldatasource/) следует рассматривать так же, как если бы это был экземпляр [DataTable](../../com.aspose.words.net.system.data/datatable/). В противном случае экземпляр [XmlDataSource](../../com.aspose.words/xmldatasource/) следует рассматривать так же, как если бы это был экземпляр [DataRow](../../com.aspose.words.net.system.data/datarow/). Для получения дополнительной информации см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Когда определение XML Schema передаётся конструктору этого класса, типы данных значений простых XML‑элементов и атрибутов определяются согласно схеме. Поэтому в шаблонных документах вы можете работать с типизированными значениями, а не только со строками.

Когда определение XML Schema не передаётся конструктору этого класса, типы данных значений простых XML‑элементов и атрибутов определяются автоматически на основе их строковых представлений. Поэтому в шаблонных документах вы также можете работать с типизированными значениями. Движок способен автоматически распознавать значения следующих типов:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Обратите внимание, что для корректной автоматической распознавания типов данных строковые представления значений простых XML‑элементов и атрибутов должны формироваться с использованием нейтральных (инвариантных) параметров культуры.

Чтобы переопределить поведение загрузки XML‑данных по умолчанию, инициализируйте и передайте экземпляр [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) конструктору этого класса.

 **Examples:** 

Покажите, как использовать XML в качестве источника данных (строка).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

Показать, как использовать XML в качестве источника данных (поток).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 InputStream stream = new FileInputStream(getMyDir() + "List of people.xml");
 try {
     XmlDataSource dataSource = new XmlDataSource(stream);
     buildReport(doc, dataSource, "persons");
 } finally {
     stream.close();
 }

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataStream.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | Создаёт новый источник данных с данными из XML‑файла, используя параметры по умолчанию для загрузки XML‑данных. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Инициализирует новый экземпляр этого класса. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | Создаёт новый источник данных с данными из XML‑файла, используя файл определения схемы XML (XSD). |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Инициализирует новый экземпляр этого класса. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Создаёт новый источник данных с данными из XML‑файла, используя указанные параметры для загрузки XML‑данных. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Инициализирует новый экземпляр этого класса. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Создаёт новый источник данных с данными из XML‑файла, используя файл определения схемы XML (XSD). |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Инициализирует новый экземпляр этого класса. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


Создаёт новый источник данных с данными из XML‑файла, используя параметры по умолчанию для загрузки XML‑данных.

 **Examples:** 

Покажите, как использовать XML в качестве источника данных (строка).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к XML‑файлу, который будет использоваться в качестве источника данных. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Создаёт новый источник данных с данными из XML‑файла, используя файл определения схемы XML. Для загрузки XML‑данных используются параметры по умолчанию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к XML‑файлу, который будет использоваться в качестве источника данных. |
| xmlSchemaPath | java.lang.String | Путь к файлу определения схемы XML, который предоставляет схему для XML‑файла. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Создаёт новый источник данных с данными из XML‑файла, используя указанные параметры для загрузки XML‑данных.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к XML‑файлу, который будет использоваться в качестве источника данных. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Параметры загрузки XML‑данных. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Создаёт новый источник данных с данными из XML‑файла, используя файл определения схемы XML. Для загрузки XML‑данных используются указанные параметры.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlPath | java.lang.String | Путь к XML‑файлу, который будет использоваться в качестве источника данных. |
| xmlSchemaPath | java.lang.String | Путь к файлу определения схемы XML, который предоставляет схему для XML‑файла. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Параметры загрузки XML‑данных. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

