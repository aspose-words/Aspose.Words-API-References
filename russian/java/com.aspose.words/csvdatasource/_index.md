---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words для Java"
description: "Обеспечивает доступ к данным CSV‑файла или потока, которые будут использоваться в отчёте на Java."
type: docs
weight: 138
url: /ru/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Обеспечивает доступ к данным CSV‑файла или потока, которые будут использоваться в отчёте.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Чтобы получить доступ к данным соответствующего файла или потока при генерации отчёта, передайте экземпляр этого класса в качестве источника данных в один из методов [ReportingEngine](../../com.aspose.words/reportingengine/). перегрузки buildReport.

В шаблонных документах экземпляр [CsvDataSource](../../com.aspose.words/csvdatasource/) следует рассматривать так же, как если бы это был экземпляр [DataTable](../../com.aspose.words.net.system.data/datatable/) . Для получения дополнительной информации см. справку по синтаксису шаблонов(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Типы данных значений, разделённых запятыми, определяются автоматически на основе их строковых представлений. Поэтому в шаблонных документах вы можете работать с типизированными значениями, а не только со строками. Движок способен автоматически распознавать значения следующих типов:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Обратите внимание, что для корректной автоматической распознавания типов данных строковые представления значений, разделённых запятыми, должны формироваться с использованием нейтральных (инвариантных) настроек культуры.

Чтобы переопределить поведение загрузки CSV‑данных по умолчанию, инициализируйте и передайте экземпляр [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) в конструктор этого класса.

 **Examples:** 

Показывает, как использовать CSV в качестве источника данных (строка).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | Создаёт новый источник данных с данными из CSV‑файла, используя параметры по умолчанию для разбора CSV‑данных. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | Создаёт новый источник данных с данными из CSV‑файла, используя указанные параметры для разбора CSV‑данных. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Инициализирует новый экземпляр этого класса. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Инициализирует новый экземпляр этого класса. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


Создаёт новый источник данных с данными из CSV‑файла, используя параметры по умолчанию для разбора CSV‑данных.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| csvPath | java.lang.String | Путь к CSV‑файлу, который будет использоваться в качестве источника данных. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Создаёт новый источник данных с данными из CSV‑файла, используя указанные параметры для разбора CSV‑данных.

 **Examples:** 

Показывает, как использовать CSV в качестве источника данных (строка).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| csvPath | java.lang.String | Путь к CSV‑файлу, который будет использоваться в качестве источника данных. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | Параметры разбора CSV‑данных. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

