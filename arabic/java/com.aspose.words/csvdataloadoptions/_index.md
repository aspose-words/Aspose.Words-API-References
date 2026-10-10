---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words لـ Java"
description: "يمثل خيارات تحليل بيانات CSV في Java."
type: docs
weight: 137
url: /ar/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

يمثل خيارات تحليل بيانات CSV.

للتعرف على المزيد، زر مقالة توثيق [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

يمكن تمرير مثال من هذه الفئة إلى مُنشئات [CsvDataSource](../../com.aspose.words/csvdatasource/).

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | يُنشئ نسخة جديدة من هذه الفئة باستخدام الخيارات الافتراضية. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | يُنشئ مثالًا جديدًا من هذه الفئة مع تحديد ما إذا كانت بيانات CSV تحتوي على أسماء الأعمدة في السطر الأول. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCommentChar()](#getCommentChar) | يحصل على الحرف المستخدم لتعليق أسطر بيانات CSV. |
| [getDelimiter()](#getDelimiter) | يحصل على الحرف الذي سيُستخدم كفاصل للأعمدة. |
| [getQuoteChar()](#getQuoteChar) | يحصل على الحرف المستخدم لتحديد قيم الحقول. |
| [hasHeaders()](#hasHeaders) | يحصل على قيمة تشير إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | يضبط قيمة تشير إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة. |
| [setCommentChar(char value)](#setCommentChar-char) | يضبط الحرف المستخدم لتعليق أسطر بيانات CSV. |
| [setDelimiter(char value)](#setDelimiter-char) | يضبط الحرف الذي سيُستخدم كفاصل للأعمدة. |
| [setQuoteChar(char value)](#setQuoteChar-char) | يضبط الحرف المستخدم لتحديد قيم الحقول. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


يُنشئ نسخة جديدة من هذه الفئة باستخدام الخيارات الافتراضية.

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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


يُنشئ مثالًا جديدًا من هذه الفئة مع تحديد ما إذا كانت بيانات CSV تحتوي على أسماء الأعمدة في السطر الأول.

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


يحصل على الحرف المستخدم لتعليق أسطر بيانات CSV.

 **Remarks:** 

القيمة الافتراضية هي '\\#' (علامة الرقم).

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
char - الحرف الذي يُستخدم لتعليق أسطر بيانات CSV.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


يحصل على الحرف الذي سيُستخدم كفاصل للأعمدة.

 **Remarks:** 

القيمة الافتراضية هي ',' (فاصلة).

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
char - الحرف الذي سيُستخدم كفاصل أعمدة.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


يحصل على الحرف المستخدم لتحديد قيم الحقول.

 **Remarks:** 

القيمة الافتراضية هي '\"' (علامة اقتباس).

ضاعف الحرف لإدراجه في نص مقتبس.

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
char - الحرف الذي يُستخدم لاقتباس قيم الحقول.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


يحصل على قيمة تشير إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
boolean - قيمة تشير إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة.

 **Remarks:** 

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كان السجل الأول لبيانات CSV يحتوي على أسماء الأعمدة. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


يضبط الحرف المستخدم لتعليق أسطر بيانات CSV.

 **Remarks:** 

القيمة الافتراضية هي '\\#' (علامة الرقم).

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | char | الحرف الذي يُستخدم لتعليق أسطر بيانات CSV. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


يضبط الحرف الذي سيُستخدم كفاصل للأعمدة.

 **Remarks:** 

القيمة الافتراضية هي ',' (فاصلة).

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | char | الحرف الذي سيُستخدم كفاصل أعمدة. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


يضبط الحرف المستخدم لتحديد قيم الحقول.

 **Remarks:** 

القيمة الافتراضية هي '\"' (علامة اقتباس).

ضاعف الحرف لإدراجه في نص مقتبس.

 **Examples:** 

يوضح كيفية استخدام CSV كمصدر بيانات (سلسلة).

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | char | الحرف الذي يُستخدم لاقتباس قيم الحقول. |

