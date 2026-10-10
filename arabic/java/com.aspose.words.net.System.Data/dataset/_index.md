---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words لـ Java"
description: "يمثل ذاكرة تخزين مؤقتة للبيانات في Java."
type: docs
weight: 24
url: /ar/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

يمثل ذاكرة تخزين مؤقتة للبيانات في الذاكرة
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DataSet()](#DataSet) | ينشئ نسخة جديدة من الفئة [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | ينشئ نسخة جديدة من الفئة DataSet مع البيانات المأخوذة من Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | ينشئ نسخة جديدة من الفئة DataSet مع البيانات المأخوذة من Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | ينشئ نسخة جديدة من الفئة [DataSet](../../com.aspose.words.net.system.data/dataset/) بالاسم المحدد. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | يمسح الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) من أي بيانات عن طريق إزالة جميع الصفوف في جميع الجداول. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | يحصل على اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) الحالي. |
| [getEnforceConstraints()](#getEnforceConstraints) | يحصل على قيمة تشير إلى ما إذا كانت قواعد القيود تُتبع عند محاولة أي عملية تحديث. |
| [getNamespace()](#getNamespace) | يحصل على مساحة الاسم للـ [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getRelations()](#getRelations) | احصل على مجموعة العلاقات التي تربط الجداول وتسمح بالتنقل من الجداول الأم إلى الجداول الفرعية. |
| [getTables()](#getTables) | يحصل على مجموعة الجداول الموجودة في الـ [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | يقرأ مخطط XML والبيانات إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) باستخدام java.io.InputStream المحدد. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | يقرأ مخطط XML والبيانات إلى الـ DataSet باستخدام java.io.InputStream المحدد و[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXml(String fileName)](#readXml-java.lang.String) | يقرأ مخطط XML والبيانات إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) باستخدام الملف المحدد. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | يقرأ مخطط XML والبيانات إلى الـ DataSet باستخدام الملف المحدد و[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | يقرأ مخطط XML من java.io.InputStream المحدد إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | يقرأ مخطط XML من الملف المحدد إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [reset()](#reset) | يعيد ضبط الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) إلى حالته الأصلية. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | يضبط اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) الحالي. |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | يضبط قيمة تشير إلى ما إذا كانت قواعد القيود تُتبع عند محاولة أي عملية تحديث. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | يضبط معلومات اللغة المستخدمة لمقارنة السلاسل داخل الجدول. |
### DataSet() {#DataSet}
```
public DataSet()
```


ينشئ نسخة جديدة من الفئة [DataSet](../../com.aspose.words.net.system.data/dataset/).

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


ينشئ نسخة جديدة من الفئة DataSet مع البيانات المأخوذة من Connection. سيتم نسخ الجداول والعلاقات والقيود والفهارس إلى DataSet.

بشكل افتراضي لن يتم استخدام أي اسم مخطط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| connection | java.sql.Connection | الذي يحتوي على بيانات قاعدة البيانات. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


ينشئ نسخة جديدة من الفئة DataSet مع البيانات المأخوذة من Connection. سيتم نسخ الجداول والعلاقات والقيود والفهارس إلى DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

أو

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| connection | java.sql.Connection | الذي يحتوي على بيانات قاعدة البيانات. |
| schemaName | java.lang.String | الذي يحتوي على الجداول التي سيتم استيرادها. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


ينشئ نسخة جديدة من الفئة [DataSet](../../com.aspose.words.net.system.data/dataset/) بالاسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dataSetName | java.lang.String | اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean - true إذا تم قراءة المخطط
### clear() {#clear}
```
public void clear()
```


يمسح الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) من أي بيانات عن طريق إزالة جميع الصفوف في جميع الجداول.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


يحصل على اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) الحالي.

**Returns:**
java.lang.String - اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


يحصل على قيمة تشير إلى ما إذا كانت قواعد القيود تُتبع عند محاولة أي عملية تحديث.

**Returns:**
boolean - true إذا تم تطبيق القواعد؛ وإلا false. الافتراضي هو true.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


يحصل على مساحة الاسم للـ [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - مساحة الاسم للـ [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


احصل على مجموعة العلاقات التي تربط الجداول وتسمح بالتنقل من الجداول الأم إلى الجداول الفرعية.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


يحصل على مجموعة الجداول الموجودة في الـ [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean - true إذا تم تعيين اللغة
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


يقرأ مخطط XML والبيانات إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) باستخدام java.io.InputStream المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream | كائن مشتق من java.io.InputStream. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


يقرأ مخطط XML والبيانات إلى الـ DataSet باستخدام java.io.InputStream المحدد و[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlStream | java.io.InputStream | المجرى الذي يُقرأ منه. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | إحدى قيم [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


يقرأ مخطط XML والبيانات إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) باستخدام الملف المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف (متضمنًا المسار) الذي يُقرأ منه. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


يقرأ مخطط XML والبيانات إلى الـ DataSet باستخدام الملف المحدد و[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xmlPath | java.lang.String | الملف المحدد |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


يقرأ مخطط XML من java.io.InputStream المحدد إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream | الـ java.io.InputStream الذي يُقرأ منه. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


يقرأ مخطط XML من الملف المحدد إلى الـ [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف (متضمنًا المسار) الذي يُقرأ منه. |

### reset() {#reset}
```
public void reset()
```


يعيد تعيين الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) إلى حالته الأصلية. يجب على الفئات الفرعية تجاوز [reset()](../../com.aspose.words.net.system.data/dataset/\\#reset) لاستعادة الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) إلى حالته الأصلية.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


يضبط اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) الحالي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | اسم الـ [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


يضبط قيمة تشير إلى ما إذا كانت قواعد القيود تُتبع عند محاولة أي عملية تحديث.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | true إذا تم تطبيق القواعد؛ وإلا false. الافتراضي هو true. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


يضبط معلومات اللغة المستخدمة لمقارنة السلاسل داخل الجدول.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| locale | java.util.Locale | من مجموعة البيانات هذه |

