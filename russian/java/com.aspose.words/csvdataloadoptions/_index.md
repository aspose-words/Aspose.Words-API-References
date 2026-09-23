---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words для Java"
description: "Представляет параметры для разбора CSV‑данных в Java."
type: docs
weight: 137
url: /ru/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Представляет параметры для разбора CSV-данных.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Экземпляр этого класса можно передать в конструкторы [CsvDataSource](../../com.aspose.words/csvdatasource/).

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
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Инициализирует новый экземпляр этого класса с параметрами по умолчанию. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Инициализирует новый экземпляр этого класса, указывая, содержит ли CSV‑данные имена столбцов в первой строке. |
## Методы

| Метод | Описание |
| --- | --- |
| [getCommentChar()](#getCommentChar) | Возвращает символ, используемый для комментирования строк CSV‑данных. |
| [getDelimiter()](#getDelimiter) | Возвращает символ, используемый в качестве разделителя столбцов. |
| [getQuoteChar()](#getQuoteChar) | Возвращает символ, используемый для заключения значений полей в кавычки. |
| [hasHeaders()](#hasHeaders) | Возвращает значение, указывающее, содержит ли первая запись CSV‑данных имена столбцов. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | Устанавливает значение, указывающее, содержит ли первая запись CSV‑данных имена столбцов. |
| [setCommentChar(char value)](#setCommentChar-char) | Устанавливает символ, используемый для комментирования строк CSV‑данных. |
| [setDelimiter(char value)](#setDelimiter-char) | Устанавливает символ, используемый в качестве разделителя столбцов. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Устанавливает символ, используемый для заключения значений полей в кавычки. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Инициализирует новый экземпляр этого класса с параметрами по умолчанию.

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

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


Инициализирует новый экземпляр этого класса, указывая, содержит ли CSV‑данные имена столбцов в первой строке.

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
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


Возвращает символ, используемый для комментирования строк CSV‑данных.

 **Remarks:** 

Значение по умолчанию — '\#' (знак решётки).

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

**Returns:**
char - Символ, который используется для комментирования строк CSV‑данных.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Возвращает символ, используемый в качестве разделителя столбцов.

 **Remarks:** 

Значение по умолчанию — ',' (запятая).

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

**Returns:**
char - Символ, используемый в качестве разделителя столбцов.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Возвращает символ, используемый для заключения значений полей в кавычки.

 **Remarks:** 

Значение по умолчанию — '"' (кавычка).

Удвоить символ, чтобы разместить его в кавычках.

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

**Returns:**
char - Символ, который используется для заключения значений полей в кавычки.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


Возвращает значение, указывающее, содержит ли первая запись CSV‑данных имена столбцов.

 **Remarks:** 

Значение по умолчанию — false.

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

**Returns:**
boolean - Значение, указывающее, содержит ли первая запись CSV‑данных имена столбцов.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


Устанавливает значение, указывающее, содержит ли первая запись CSV‑данных имена столбцов.

 **Remarks:** 

Значение по умолчанию — false.

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
| значение | boolean | Значение, указывающее, содержит ли первая запись CSV‑данных имена столбцов. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


Устанавливает символ, используемый для комментирования строк CSV‑данных.

 **Remarks:** 

Значение по умолчанию — '\#' (знак решётки).

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
| значение | char | Символ, который используется для комментирования строк CSV‑данных. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Устанавливает символ, используемый в качестве разделителя столбцов.

 **Remarks:** 

Значение по умолчанию — ',' (запятая).

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
| значение | char | Символ, используемый в качестве разделителя столбцов. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Устанавливает символ, используемый для заключения значений полей в кавычки.

 **Remarks:** 

Значение по умолчанию — '"' (кавычка).

Удвоить символ, чтобы разместить его в кавычках.

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
| значение | char | Символ, который используется для заключения значений полей в кавычки. |

