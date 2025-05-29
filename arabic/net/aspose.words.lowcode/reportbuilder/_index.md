---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words لـ .NET
description: أنشئ تقارير ديناميكية بسهولة باستخدام Aspose.Words LowCode ReportBuilder. استخدم محرك تقارير LINQ لملء القوالب بالبيانات بسلاسة.
type: docs
weight: 4360
url: /ar/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

يوفر طرقًا مخصصة لملء القالب بالبيانات باستخدام محرك التقارير LINQ.

```csharp
public class ReportBuilder : Processor
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | ينشئ مثيلًا جديدًا لمعالج إنشاء التقارير. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | ينشئ مثيلًا جديدًا لمعالج إنشاء التقارير. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | تنفيذ إجراء المعالج. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد ملف الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد ملف الإخراج للمعالج. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل مع خيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية، من تدفقات الإدخال والإخراج. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية، من تدفقات الإدخال والإخراج. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل مع مرجع مصدر بيانات مسمى وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة، مما يؤدي إلى إنشاء تقرير مكتمل بخيارات إضافية. يحدد هذا التحميل الزائد تنسيق الحفظ تلقائيًا استنادًا إلى امتداد ملف الإخراج. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل مع مرجع مصدر بيانات مسمى وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية من تدفقات ملفات الإدخال والإخراج المحددة. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل مع مرجع مصدر بيانات مسمى وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية من تدفقات ملفات الإدخال والإخراج المحددة. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد، ومرجع مصدر بيانات مسمى، وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من المصدر المحدد، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد، ومرجع مصدر بيانات مسمى، وخيارات إضافية. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة، مما يؤدي إلى إنشاء تقرير مكتمل بتنسيق إخراج محدد وخيارات إضافية. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة. يعرض الإخراج على شكل صور. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | يملأ مستند القالب بالبيانات من مصادر متعددة. يعرض الإخراج على شكل صور. |

### أنظر أيضا

* class [Processor](../processor/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
