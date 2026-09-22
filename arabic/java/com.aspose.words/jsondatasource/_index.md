---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words لـ Java"
description: "يوفر إمكانية الوصول إلى بيانات ملف JSON أو تدفق لاستخدامها داخل تقرير في Java."
type: docs
weight: 409
url: /ar/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

يوفر الوصول إلى بيانات ملف JSON أو الدفق لاستخدامها داخل تقرير.

للتعرف على المزيد، زر مقالة توثيق [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

للوصول إلى بيانات الملف أو التدفق المقابل أثناء إنشاء تقرير، مرّر نسخة من هذه الفئة كمصدر بيانات إلى أحد إصدارات [ReportingEngine](../../com.aspose.words/reportingengine/). الإصدارات المتعددة لـ buildReport.

في مستندات القالب، إذا كان عنصر JSON من المستوى الأعلى مصفوفة، يجب التعامل مع نسخة من [JsonDataSource](../../com.aspose.words/jsondatasource/) كما لو كانت نسخة من [DataTable](../../com.aspose.words.net.system.data/datatable/). إذا كان عنصر JSON من المستوى الأعلى كائنًا، يجب التعامل مع نسخة من [JsonDataSource](../../com.aspose.words/jsondatasource/) كما لو كانت نسخة من [DataRow](../../com.aspose.words.net.system.data/datarow/). لمزيد من المعلومات، راجع مرجع صياغة القالب (https://docs.aspose.com/display/wordsjava/Template+Syntax).

في مستندات القالب، يمكنك العمل مع القيم ذات النوع لعناصر JSON. لتسهيل الأمر، يستبدل المحرك مجموعة الأنواع البسيطة لـ JSON بالنوع التالي:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

يتعرف المحرك تلقائيًا على قيم الأنواع الإضافية بناءً على تمثيلاتها في JSON.

لتجاوز السلوك الافتراضي لتحميل بيانات JSON، قم بتهيئة وتمرير نسخة من [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) إلى مُنشئ هذه الفئة.

 **Examples:** 

يوضح كيفية استخدام JSON كمصدر بيانات (سلسلة).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | ينشئ مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | ينشئ مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات المحددة لتحليل بيانات JSON. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


ينشئ مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات الافتراضية لتحليل بيانات JSON.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| jsonPath | java.lang.String | المسار إلى ملف JSON الذي سيُستخدم كمصدر للبيانات. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


ينشئ مصدر بيانات جديد ببيانات من ملف JSON باستخدام الخيارات المحددة لتحليل بيانات JSON.

 **Examples:** 

يوضح كيفية استخدام JSON كمصدر بيانات (سلسلة).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| jsonPath | java.lang.String | المسار إلى ملف JSON الذي سيُستخدم كمصدر للبيانات. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | خيارات تحليل بيانات JSON. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

