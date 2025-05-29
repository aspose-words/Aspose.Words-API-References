---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words لـ .NET
description: أطلق العنان لتقاريرك الفعّالة مع Aspose.Words.XmlDataSource. تمكّن من الوصول بسهولة إلى بيانات XML لدمجها بسلاسة في تقاريرك وتحسين عرض البيانات.
type: docs
weight: 5490
url: /ar/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

يوفر الوصول إلى بيانات ملف XML أو مجرى البيانات المراد استخدامه داخل التقرير.

لمعرفة المزيد، قم بزيارة[محرك إعداد التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class XmlDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | ينشئ مصدر بيانات جديد باستخدام البيانات من مجرى XML باستخدام الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | ينشئ مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | يُنشئ مصدر بيانات جديدًا ببيانات من دفق XML باستخدام دفق تعريف مخطط XML. تُستخدم الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | ينشئ مصدر بيانات جديد باستخدام البيانات من مجرى XML باستخدام الخيارات المحددة لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | يُنشئ مصدر بيانات جديد ببيانات من ملف XML باستخدام ملف تعريف مخطط XML. تُستخدم الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | ينشئ مصدر بيانات جديد بالبيانات من ملف XML باستخدام الخيارات المحددة لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | يُنشئ مصدر بيانات جديدًا ببيانات من دفق XML باستخدام دفق تعريف مخطط XML. تُستخدم خيارات specific لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | يُنشئ مصدر بيانات جديدًا ببيانات من ملف XML باستخدام ملف تعريف مخطط XML. تُستخدم خيارات specific لتحميل بيانات XML. |

## ملاحظات

للوصول إلى بيانات الملف أو التدفق المقابل أثناء إنشاء تقرير، مرر مثيلًا لهذه الفئة as مصدر بيانات إلى أحد[`ReportingEngine`](../reportingengine/) .BuildReport overloads.

في مستندات القالب، إذا كان عنصر XML من المستوى الأعلى يحتوي فقط على قائمة من العناصر من نفس النوع، `XmlDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataTable مثال. وإلا،`XmlDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataRow مثال . لمزيد من المعلومات، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

عند تمرير تعريف مخطط XML إلى مُنشئ من هذه الفئة، تُحدَّد أنواع بيانات قيم عناصر XML البسيطة والسمات وفقًا للمخطط. لذا، في مستندات القالب، يمكنك العمل مع القيم المكتوبة (x000d) بدلاً من السلاسل النصية فقط.

عند عدم تمرير تعريف مخطط XML إلى مُنشئ هذه الفئة، تُحدَّد أنواع بيانات قيم عناصر XML البسيطة والسمات تلقائيًا بناءً على تمثيلاتها النصية. لذا، في مستندات القالب، يمكنك استخدام مع القيم المكتوبة في هذه الحالة أيضًا. يستطيع المُحرِّك التعرف تلقائيًا على قيم الأنواع التالية:

* Nullable
* Nullable
* Nullable
* Nullable
* String

لاحظ أنه لكي يعمل التعرف التلقائي على أنواع البيانات، يجب تشكيل تمثيلات سلسلة لقيم عناصر XML البسيطة والسمات باستخدام إعدادات الثقافة الثابتة.

لتجاوز السلوك الافتراضي لتحميل بيانات XML، قم بتهيئة وتمرير[`XmlDataLoadOptions`](../xmldataloadoptions/) مثيل لمنشئ هذه الفئة.

## أمثلة

إظهار كيفية استخدام XML كمصدر للبيانات (سلسلة).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

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

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
