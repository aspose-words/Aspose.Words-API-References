---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words لـ .NET
description: قسّم المستندات بسهولة باستخدام فئة Aspose.Words.LowCode.Splitter. استخدم أساليب متعددة لإدارة المستندات بدقة وكفاءة أعلى في سير العمل.
type: docs
weight: 4420
url: /ar/net/aspose.words.lowcode/splitter/
---
## Splitter class

يوفر طرقًا تهدف إلى تقسيم المستندات إلى أجزاء باستخدام معايير مختلفة.

```csharp
public class Splitter : Processor
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | ينشئ مثيلًا جديدًا لمعالج التقسيم. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | تنفيذ إجراء المعالج. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد ملف الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد ملف الإخراج للمعالج. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند، ويحفظها في ملف جديد. يُحدَّد تنسيق ملف الإخراج بامتداد اسم الملف. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | يستخرج نطاقًا محددًا من الصفحات من مجرى مستند ويحفظ الصفحات المستخرجة في مجرى إخراج باستخدام تنسيق الحفظ المحدد. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | يستخرج نطاقًا محددًا من الصفحات من مجرى مستند ويحفظ الصفحات المستخرجة في مجرى إخراج باستخدام تنسيق الحفظ المحدد. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | يزيل الصفحات الفارغة من المستند ويحفظ النتيجة. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يزيل الصفحات الفارغة من مستند مُقدَّم في مسار إدخال، ويحفظ المستند المُحدَّث في مسار إخراج بتنسيق الحفظ المُحدَّد. يُرجع قائمة بأرقام الصفحات التي حُذفت. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يزيل الصفحات الفارغة من مستند مُقدَّم في مسار إدخال، ويحفظ المستند المُحدَّث في مسار إخراج بتنسيق الحفظ المُحدَّد. يُرجع قائمة بأرقام الصفحات التي حُذفت. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | يزيل الصفحات الفارغة من المستند ويحفظ الناتج بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يزيل الصفحات الفارغة من المستند ويحفظ الناتج بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | يقوم بتقسيم مستند من مجرى إدخال إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويقوم بإرجاع الأجزاء الناتجة كمجموعة من المجاري بتنسيق الحفظ المحدد. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | يقوم بتقسيم مستند من مجرى إدخال إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويقوم بإرجاع الأجزاء الناتجة كمجموعة من المجاري بتنسيق الحفظ المحدد. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | يُقسّم المستند إلى أجزاء متعددة بناءً على خيارات التقسيم المُحددة، ويحفظ الأجزاء الناتجة في ملفات. يُحدَّد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | يقسم المستند إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات بتنسيق الحفظ المحدد. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | يقسم المستند إلى أجزاء متعددة استنادًا إلى خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات بتنسيق الحفظ المحدد. |

### أنظر أيضا

* class [Processor](../processor/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
