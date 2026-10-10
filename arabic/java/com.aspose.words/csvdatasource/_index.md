---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words لـ Java"
description: "يوفر الوصول إلى بيانات ملف CSV أو تدفق لاستخدامها داخل تقرير في Java."
type: docs
weight: 138
url: /ar/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

يوفر الوصول إلى بيانات ملف CSV أو تدفق لاستخدامها داخل تقرير.

للتعرف على المزيد، زر مقالة توثيق [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

للوصول إلى بيانات الملف أو التدفق المقابل أثناء إنشاء تقرير، مرّر نسخة من هذه الفئة كمصدر بيانات إلى أحد إصدارات [ReportingEngine](../../com.aspose.words/reportingengine/). الإصدارات المتعددة لـ buildReport.

في مستندات القالب، يجب التعامل مع مثيل [CsvDataSource](../../com.aspose.words/csvdatasource/) كما لو كان مثيلًا لـ [DataTable](../../com.aspose.words.net.system.data/datatable/) . لمزيد من المعلومات، راجع مرجع بناء القالب(https://docs.aspose.com/display/wordsjava/Template+Syntax).

يتم تحديد أنواع القيم المفصولة بفواصل تلقائيًا بناءً على تمثيلها النصي. لذلك في مستندات القالب، يمكنك العمل مع قيم ذات نوع بدلاً من مجرد سلاسل نصية. المحرك قادر على التعرف تلقائيًا على القيم من الأنواع التالية:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

لاحظ أنه لكي يعمل التعرف التلقائي على أنواع البيانات، يجب تكوين تمثيلات السلاسل للقيم المفصولة بفواصل باستخدام إعدادات ثقافة ثابتة.

لتجاوز السلوك الافتراضي لتحميل بيانات CSV، قم بتهيئة وتمرير مثيل [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) إلى مُنشئ هذه الفئة.

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
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | ينشئ مصدر بيانات جديد ببيانات من ملف CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | ينشئ مصدر بيانات جديد ببيانات من ملف CSV باستخدام الخيارات المحددة لتحليل بيانات CSV. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


ينشئ مصدر بيانات جديد ببيانات من ملف CSV باستخدام الخيارات الافتراضية لتحليل بيانات CSV.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| csvPath | java.lang.String | المسار إلى ملف CSV الذي سيُستخدم كمصدر للبيانات. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


ينشئ مصدر بيانات جديد ببيانات من ملف CSV باستخدام الخيارات المحددة لتحليل بيانات CSV.

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
| csvPath | java.lang.String | المسار إلى ملف CSV الذي سيُستخدم كمصدر للبيانات. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | خيارات تحليل بيانات CSV. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

