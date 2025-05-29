---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words لـ .NET
description: أطلق العنان لأتمتة المستندات القوية مع Aspose.Words.ReportingEngine. املأ القوالب بالبيانات بسهولة، وخصّص الإعدادات لإعداد تقارير سلسة.
type: docs
weight: 5470
url: /ar/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

يوفر روتينات لملء مستندات القالب بالبيانات ومجموعة من الإعدادات للتحكم في هذه الروتينات.

لمعرفة المزيد، قم بزيارة[محرك إعداد التقارير LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) مقالة توثيقية.

```csharp
public class ReportingEngine
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ReportingEngine](reportingengine/)() | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | يحصل على مجموعة غير مرتبة (أي مجموعة من العناصر الفريدة) تحتوي علىType الكائنات التي يمكن استخدام أسمائها المؤهلة بالكامل أو جزئيًا داخل قوالب التقارير التي تتم معالجتها بواسطة مثيل engine هذا لاستدعاء الأعضاء الثابتة للأنواع المقابلة، وإجراء عمليات تحويل النوع، وما إلى ذلك. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | يحصل على أو يعيّن قيمة سلسلة نصية مطبوعة بدلاً من تعبير قالب يمثل مرجعًا بسيطًا إلى ، وهو عنصر مفقود في كائن. القيمة الافتراضية هي سلسلة نصية فارغة. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | يحصل على مجموعة من العلامات التي تتحكم في سلوك هذا أو يعينها`ReportingEngine` مثال أثناء بناء تقرير. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | يحصل على قيمة أو يعيّنها لتحديد ما إذا كانت استدعاءات عناصر النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد الفئات الديناميكي أم لا. القيمة الافتراضية هي`حقيقي` . |

## طُرق

| اسم | وصف |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | يملأ مستند القالب المحدد بالبيانات من المصادر المحددة مما يجعله تقريرًا جاهزًا. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | يعيد الأنواع، وأي الأعضاء، وكذلك أعضاء الأنواع المشتقة التي يجب ألا يتمكن engine من الوصول إليها من خلال بناء جملة القالب. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | يحدد الأنواع، وأي الأعضاء، وكذلك أعضاء الأنواع المشتقة التي يجب ألا يتمكن engine من الوصول إليها من خلال بناء جملة القالب. |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
