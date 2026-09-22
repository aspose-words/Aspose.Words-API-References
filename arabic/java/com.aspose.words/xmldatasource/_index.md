---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words لـ Java"
description: "يوفر إمكانية الوصول إلى بيانات ملف XML أو تدفق لاستخدامها داخل تقرير في Java."
type: docs
weight: 746
url: /ar/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

يوفر الوصول إلى بيانات ملف XML أو تدفق لاستخدامها داخل تقرير.

للتعرف على المزيد، زر مقالة توثيق [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

للوصول إلى بيانات الملف أو التدفق المقابل أثناء إنشاء تقرير، مرّر نسخة من هذه الفئة كمصدر بيانات إلى أحد إصدارات [ReportingEngine](../../com.aspose.words/reportingengine/). الإصدارات المتعددة لـ buildReport.

في مستندات القالب، إذا كان عنصر XML من المستوى الأعلى يحتوي فقط على قائمة من العناصر من نفس النوع، يجب التعامل مع كائن [XmlDataSource](../../com.aspose.words/xmldatasource/) كما لو كان كائنًا من نوع [DataTable](../../com.aspose.words.net.system.data/datatable/) . وإلا، يجب التعامل مع كائن [XmlDataSource](../../com.aspose.words/xmldatasource/) كما لو كان كائنًا من نوع [DataRow](../../com.aspose.words.net.system.data/datarow/) . لمزيد من المعلومات، راجع مرجع بناء جملة القالب(https://docs.aspose.com/display/wordsjava/Template+Syntax).

عند تمرير تعريف مخطط XML (XML Schema Definition) إلى مُنشئ هذه الفئة، يتم تحديد أنواع البيانات لقيم عناصر XML البسيطة والسمات وفقًا للمخطط. لذا في مستندات القالب، يمكنك العمل بالقيم ذات النوع بدلاً من السلاسل النصية فقط.

عند عدم تمرير تعريف مخطط XML إلى مُنشئ هذه الفئة، يتم تحديد أنواع البيانات لقيم عناصر XML البسيطة والسمات تلقائيًا بناءً على تمثيلها النصي. لذا في مستندات القالب، يمكنك أيضًا العمل بالقيم ذات النوع في هذه الحالة. المحرك قادر على التعرف تلقائيًا على القيم من الأنواع التالية:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

لاحظ أنه لكي يعمل التعرف التلقائي على أنواع البيانات، يجب تشكيل تمثيلات السلاسل النصية لقيم عناصر XML البسيطة والسمات باستخدام إعدادات ثقافة ثابتة.

لتجاوز السلوك الافتراضي لتحميل بيانات XML، قم بتهيئة وتمرير كائن [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) إلى مُنشئ هذه الفئة.

 **Examples:** 

يوضح كيفية استخدام XML كمصدر للبيانات (سلسلة).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

عرض كيفية استخدام XML كمصدر للبيانات (تدفق).

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام ملف تعريف مخطط XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات المحددة لتحميل بيانات XML. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام ملف تعريف مخطط XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات الافتراضية لتحميل بيانات XML.

 **Examples:** 

يوضح كيفية استخدام XML كمصدر للبيانات (سلسلة).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlPath | java.lang.String | المسار إلى ملف XML الذي سيُستخدم كمصدر للبيانات. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام ملف تعريف مخطط XML. تُستخدم الخيارات الافتراضية لتحميل بيانات XML.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlPath | java.lang.String | المسار إلى ملف XML الذي سيُستخدم كمصدر للبيانات. |
| xmlSchemaPath | java.lang.String | المسار إلى ملف تعريف مخطط XML الذي يوفر المخطط لملف XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات المحددة لتحميل بيانات XML.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlPath | java.lang.String | المسار إلى ملف XML الذي سيُستخدم كمصدر للبيانات. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | خيارات تحميل بيانات XML. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


إنشاء مصدر بيانات جديد بالبيانات من ملف XML باستخدام ملف تعريف مخطط XML. تُستخدم الخيارات المحددة لتحميل بيانات XML.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlPath | java.lang.String | المسار إلى ملف XML الذي سيُستخدم كمصدر للبيانات. |
| xmlSchemaPath | java.lang.String | المسار إلى ملف تعريف مخطط XML الذي يوفر المخطط لملف XML. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | خيارات تحميل بيانات XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

