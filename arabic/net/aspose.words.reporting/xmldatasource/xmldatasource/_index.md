---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words لـ .NET
description: قم بإنشاء مصدر بيانات قوي بسهولة باستخدام منشئ XmlDataSource، وتحميل بيانات XML باستخدام خيارات افتراضية محسّنة للتكامل السلس.
type: docs
weight: 10
url: /ar/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

ينشئ مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات الافتراضية لتحميل بيانات XML.

```csharp
public XmlDataSource(string xmlPath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlPath | String | المسار إلى ملف XML الذي سيتم استخدامه كمصدر للبيانات. |

## أمثلة

إظهار كيفية استخدام XML كمصدر للبيانات (سلسلة).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### أنظر أيضا

* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

ينشئ مصدر بيانات جديد باستخدام البيانات من مجرى XML باستخدام الخيارات الافتراضية لتحميل بيانات XML.

```csharp
public XmlDataSource(Stream xmlStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlStream | Stream | تدفق بيانات XML الذي سيتم استخدامه كمصدر للبيانات. |

## أمثلة

إظهار كيفية استخدام XML كمصدر للبيانات (دفق).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### أنظر أيضا

* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

يُنشئ مصدر بيانات جديد ببيانات من ملف XML باستخدام ملف تعريف مخطط XML. تُستخدم الخيارات الافتراضية لتحميل بيانات XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlPath | String | المسار إلى ملف XML الذي سيتم استخدامه كمصدر للبيانات. |
| xmlSchemaPath | String | المسار إلى ملف تعريف مخطط XML الذي يوفر مخططًا لملف XML . |

### أنظر أيضا

* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

يُنشئ مصدر بيانات جديدًا ببيانات من دفق XML باستخدام دفق تعريف مخطط XML. تُستخدم الخيارات الافتراضية لتحميل بيانات XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlStream | Stream | تدفق بيانات XML الذي سيتم استخدامه كمصدر للبيانات. |
| xmlSchemaStream | Stream | تدفق تعريف مخطط XML الذي يوفر مخططًا لبيانات XML. |

### أنظر أيضا

* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

ينشئ مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات المحددة لتحميل بيانات XML.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlPath | String | المسار إلى ملف XML الذي سيتم استخدامه كمصدر للبيانات. |
| options | XmlDataLoadOptions | خيارات لتحميل بيانات XML. |

### أنظر أيضا

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

ينشئ مصدر بيانات جديد باستخدام البيانات من مجرى XML باستخدام الخيارات المحددة لتحميل بيانات XML.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlStream | Stream | تدفق بيانات XML الذي سيتم استخدامه كمصدر للبيانات. |
| options | XmlDataLoadOptions | خيارات لتحميل بيانات XML. |

### أنظر أيضا

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

يُنشئ مصدر بيانات جديدًا ببيانات من ملف XML باستخدام ملف تعريف مخطط XML. تُستخدم خيارات specific لتحميل بيانات XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlPath | String | المسار إلى ملف XML الذي سيتم استخدامه كمصدر للبيانات. |
| xmlSchemaPath | String | المسار إلى ملف تعريف مخطط XML الذي يوفر مخططًا لملف XML . |
| options | XmlDataLoadOptions | خيارات لتحميل بيانات XML. |

### أنظر أيضا

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

يُنشئ مصدر بيانات جديدًا ببيانات من دفق XML باستخدام دفق تعريف مخطط XML. تُستخدم خيارات specific لتحميل بيانات XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| xmlStream | Stream | تدفق بيانات XML الذي سيتم استخدامه كمصدر للبيانات. |
| xmlSchemaStream | Stream | تدفق تعريف مخطط XML الذي يوفر مخططًا لبيانات XML. |
| options | XmlDataLoadOptions | خيارات لتحميل بيانات XML. |

### أنظر أيضا

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
