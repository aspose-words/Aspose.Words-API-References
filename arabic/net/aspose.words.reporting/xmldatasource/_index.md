---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Reporting.XmlDataSource فصل. يوفر الوصول إلى بيانات ملف XML أو الدفق لاستخدامه في التقرير في C#.
type: docs
weight: 4750
url: /ar/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

يوفر الوصول إلى بيانات ملف XML أو الدفق لاستخدامه في التقرير.

لمعرفة المزيد، قم بزيارة[محرك التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class XmlDataSource
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | إنشاء مصدر بيانات جديد ببيانات من تدفق XML باستخدام الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | إنشاء مصدر بيانات جديد ببيانات من ملف XML باستخدام الخيارات الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | إنشاء مصدر بيانات جديد ببيانات من دفق XML باستخدام دفق تعريف مخطط XML. يتم استخدام options الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | إنشاء مصدر بيانات جديد ببيانات من تدفق XML باستخدام الخيارات المحددة لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | إنشاء مصدر بيانات جديد ببيانات من ملف XML باستخدام ملف تعريف مخطط XML. يتم استخدام options الافتراضية لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | إنشاء مصدر بيانات جديد ببيانات من ملف XML باستخدام الخيارات المحددة لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | إنشاء مصدر بيانات جديد ببيانات من دفق XML باستخدام دفق تعريف مخطط XML. يتم استخدام الخيارات المحددة لتحميل بيانات XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | إنشاء مصدر بيانات جديد ببيانات من ملف XML باستخدام ملف تعريف مخطط XML. يتم استخدام الخيارات المحددة لتحميل بيانات XML. |

## ملاحظات

للوصول إلى بيانات الملف أو الدفق المقابل أثناء إنشاء تقرير، قم بتمرير مثيل من هذه الفئة as مصدر بيانات إلى أحدها[`ReportingEngine`](../reportingengine/) .BuildReport الحمولة الزائدة.

في مستندات القالب، إذا كان عنصر XML ذو المستوى الأعلى يحتوي فقط على قائمة عناصر من نفس النوع، an`XmlDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataTable مثيل. خلاف ذلك، أ`XmlDataSource` يجب التعامل مع المثيل بنفس الطريقة كما لو كان aDataRow مثيل. لمزيد من المعلومات، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

عندما يتم تمرير تعريف مخطط XML إلى مُنشئ هذه الفئة، يتم تحديد أنواع البيانات وقيم عناصر XML البسيطة والسمات وفقًا للمخطط. لذا، في مستندات النماذج، يمكنك العمل باستخدام القيم المكتوبة بدلاً من السلاسل فقط.

عندما لا يتم تمرير تعريف مخطط XML إلى مُنشئ هذه الفئة، يتم تحديد أنواع بيانات قيم عناصر XML البسيطة والسمات تلقائيًا بناءً على تمثيلات السلسلة الخاصة بها. لذا، في مستندات القالب، يمكنك العمل مع القيم المكتوبة في هذه الحالة أيضًا. المحرك قادر على التعرف تلقائيًا على قيم الأنواع التالية:

* Nullable
* Nullable
* Nullable
* Nullable
* String

لاحظ أنه لكي يعمل التعرف التلقائي على أنواع البيانات، يجب تشكيل تمثيلات سلسلة لقيم عناصر XML البسيطة والسمات باستخدام إعدادات الثقافة الثابتة.

لتجاوز السلوك الافتراضي لتحميل بيانات XML، قم بتهيئة وتمرير ملف[`XmlDataLoadOptions`](../xmldataloadoptions/) مثيل لمنشئ هذه الفئة.

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
